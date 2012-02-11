---
layout: post
title: "Machinist and Association Validations"
date: 2012-02-11 11:32
comments: true
categories:
---

While upgrading to Machinist 2, I had a heck of a time getting blueprints with associations to actually save.

The problem turned out to be that the code was using `validates_presence_of :hometown_id`, where `hometown` is the name of the association, and the solution is to use `validates_presence_of :hometown`, or the newer version: `validates :hometown, presence: true`.

If you have a given class:

``` ruby
class Viking < ActiveRecord::Base
  belongs_to :hometown

  validates_presence_of :hometown_id
end
```

and blueprints:
``` ruby
Viking.blueprint do
  name { "Heiðrek" }
  hometown
end
```

Then calling `Viking.make` will properly return an unsaved Viking object (with a Hometown object `viking.hometown`), but `valid?` will return false.

Calling `Viking.make!` will throw an exception: `ActiveRecord::RecordInvalid: Validation failed: Hometown can't be blank`

If you really want to keep using `validates_presence_of :hometown_id`, you can modify the blueprint like this:
``` ruby
Viking.blueprint do
  name { "Heiðrek" }
  hometown { Hometown.make! }
end
```

Then Viking.make! will succeed. Viking.make will also work, and will return an unsaved Viking object, but it will actually create and save the associated Hometown object, which negates part of the point of calling `.make` instead of `.make!` (`make` creates objects but does not save them to the database, giving quite a performance boost for test suites).

The proper solution is to adjust the validation in your model:

``` ruby
class Viking < ActiveRecord::Base
  belongs_to :hometown

  validates :hometown, presence: true
  validates_associated :hometown
end
```

The key is that we've changed `validates_presence_of :hometown_id` to `validates :hometown, presence: true`. The validation actually checks the association itself, not the presence of an id field (which is only ever set once the hometown is saved).

We've also added a `validates_associated :hometown` call, which will check `hometown.valid?` before saving, and if the hometown fails validation, then the viking object will as well.

See API docs about validations here:

 * [validates](http://api.rubyonrails.org/classes/ActiveModel/Validations/ClassMethods.html#method-i-validates)
 * [validates_associated](http://api.rubyonrails.org/classes/ActiveRecord/Validations/ClassMethods.html#method-i-validates_associated)
