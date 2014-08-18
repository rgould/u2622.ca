---
layout: post
title: "Disadvantages of using Meteor (over Rails)"
date: 2014-08-24 20:22:26 -0700
comments: true
categories: meteor
---

You can save significant amounts of time by developing some web applications by using Meteor instead of Ruby on Rails, but it doesn't come without drawbacks. Here are some of the ones that I've encountered:
What are the disadvantages of using Meteor compared to Ruby on Rails?

**Immature Environment**: The biggest problem right now is that Meteor is new. Pretty much brand new, in the scope of web development. It's not even version 1.0 yet, though it's getting close. This means that it doesn't have as many users, as many tutorials, as many books, as many screencasts. It can be hard if you run into a problem that no one else has run into yet, so you'll need to be willing to dig into it a bit yourself. I've been there, and fortunately Meteor's codebase is fairly cleanly written (especially compared to Rails and AngularJS, two other frameworks whose code I've read).

**Not Widely Supported**: Another consequence of being so new is that there aren't as many hosting services available for Meteor apps yet. It is possible to deploy Meteor on Heroku, and in my experience it works well, though it feels very raw.

**Nothing but JavaScript**: You must run JavaScript (or Coffeescript) on the server side. This isn't a big deal for me, but JS is definitely far from the first language I would choose to work with. The upside is that you can run the same code on the server and the browser, without worrying about having to cross-compile from another language.

**Only MongoDB**: As of now, the only supported database is MongoDB. They have plans to expand this in the future.

**Rapidly Changing**: The Meteor API is rapidly changing, so each new minor version may bring breaking changes. This is expected to lessen as it reaches 1.0.

**Testing Frameworks**: Testing frameworks haven't been a high priority since the beginning, and the ones available so far have tended to be cumbersome and brittle. The community is working on solutions, but nothing stable has yet emerged, and the testing culture is nothing like the Ruby on Rails community's.

What are some other disadvantages you can think of? Email me or leave a comment!
