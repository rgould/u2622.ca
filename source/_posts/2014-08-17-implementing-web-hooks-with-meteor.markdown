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
