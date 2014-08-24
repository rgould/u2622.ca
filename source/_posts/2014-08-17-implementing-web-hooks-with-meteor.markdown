---
layout: post
title: "Implementing web hooks with Meteor"
date: 2014-08-17 19:21
comments: true
categories: meteor
---

It's possible to add web hooks to your Meteor application by using iron-router.

Declare a server-side route in your Routes.map declaration:

``` javascript
    Router.map(function() {
      ... // Your other routes go here

      this.route('hook', {
        path: '/hook',
        where: 'server',
        action: function() {

          // Watch the Meteor log to see this output
          console.log("Hook called.");
          console.log("Headers: ", this.request.headers);
          console.log("Data: ", this.request.body);

          this.response.writeHead(200, {'Content-Type': 'text/html'});
          this.response.write("You wrote: " + this.request.body.message);
          this.response.write("\n");

          // `this.response.end` *must* be called, or else the connection is left open.
          this.response.end('Success!\n');
        }
      });

    });
```

To test it out, issue this curl command from the command line:

``` bash
    curl -H "Content-Type: application/json" -d '{"message":"foo"}' http://localhost:3000/hook
```

The documentation for `this.response` and `this.request` are available on the node.js website: http://nodejs.org/api/http.html

I've created a sample Meteor application demonstrating this, which you can view at https://github.com/rgould/meteor-posthooks

Not clear enough? Send me an email at rgould@u2622.ca for some more help!

<!-- Begin MailChimp Signup Form -->
<link href="//cdn-images.mailchimp.com/embedcode/slim-081711.css" rel="stylesheet" type="text/css">
<style type="text/css">
  #mc_embed_signup{background:#fff; clear:left; font:14px Helvetica,Arial,sans-serif; }
  /* Add your own MailChimp form style overrides in your site stylesheet or in this style block.
     We recommend moving this block and the preceding CSS link to the HEAD of your HTML file. */
</style>
<div id="mc_embed_signup">
<form action="//wordpress.us8.list-manage.com/subscribe/post?u=ff25df46443f09aa393c2ae1d&amp;id=46f2ebecac" method="post" id="mc-embedded-subscribe-form" name="mc-embedded-subscribe-form" class="validate" target="_blank" novalidate>
  <label for="mce-EMAIL">Don't miss out on my next post!</label>
  <input type="email" value="" name="EMAIL" class="email" id="mce-EMAIL" placeholder="email address" required>
    <!-- real people should not fill this in and expect good things - do not remove this or risk form bot signups-->
    <div style="position: absolute; left: -5000px;"><input type="text" name="b_ff25df46443f09aa393c2ae1d_46f2ebecac" tabindex="-1" value=""></div>
    <div class="clear"><input type="submit" value="Subscribe" name="subscribe" id="mc-embedded-subscribe" class="button"></div>
</form>
</div>

<!--End mc_embed_signup-->
