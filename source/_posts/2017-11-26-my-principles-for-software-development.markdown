---
layout: post
title: "My Principles for Software Development"
date: 2017-11-26 18:37:38 +0100
comments: true
categories:
---

Here are some of the principles by which I try to develop software. This isn't
a hard-and-fast list, but rather a set of guidelines that I use. I don't follow
all of them every day, but I try to follow them as much as I can. This list is
under constant review, extending and changing as I grow as a developer.

* **Don't leave work unfinished** - Work that is started but not finished is a
    liability. At best, it means a feature isn't in production sooner than it
    could be (representing wasted opportunity). At worst, the feature will
    suffer from [software rot], and may require substantial rewriting if left
    long enough.

* **Work on only one thing at a time** - Mental context switching is expensive.
    Focus as much as possible until that item is done.

* **Teamwork** - The team as a whole is more important than the individual.
    This means that you should write maintainable code, ask for help when you
    get stuck, and help out your colleagues when they need it.

* **Review pull requests** thoroughly and in a timely manner - as part of teamwork and
    leaving work unfinished, review your colleagues' work quickly. If they write
    a PR and it sits for a week, that is means it takes one week longer for that
    feature to make it into production.

* **Fix bugs first** - Bugs should be fixed before anything else. They are easier
    to fix when fresh, and existing bugs represent potential bad experience for
    enduser. See the [Pragmatic Programmers' broken window theory][broken window].

* **Be aware of errors** - Whenever an error or problem occurs, we must be
    notified of it. Otherwise, only users will experience it, and not all users
    report errors. Also if a bug is fixed before a user first notices, the bug
    doesn't exist from their perspective. An app slowing down to unusable
    speeds is considered a bug.

* **Don't live with pain** - When something is frustrating, take the time to
    fix the problem for everyone. Automate common tasks. This makes life easier,
    and makes the software easier to work with. It's not always possible given
    time contraints, but it's worth it. This is how big things such as Rails or
    Meteor get built.

* **Produce high quality code** - Take the time to do things correctly. Quality
    is worth it.

* **Be pragmatic (but balance ideals)** - Striving for ideals is fantastic, but
    shipping usable code is the most important.

* **Don't let email/requests go unanswered** - Others have taken the time to
    ask something of you. Be courteous, and don't make them wait.

* **Provide test coverage** - Do this where possible. The value it provides is
    tremendous. Try to consider a feature to be complete when it has test
    coverage.

* **Keep learning** - Always be trying to learn new things. This includes new
    ways to use existing tools, or new tools altogether. Tools range from
    programming languages, frameworks, paradigms, editors, to soft skills such
    as empathy and listening skills.

* **Blame problems not people** - Don't forget that code is written by humans,
    with real feelings. Focus on the problem itself; blaming the author is
    counterproductive.

* **Encourage, don't discourage** - Help others improve their code. Don't put
    them down because they wrote code that you (subjectively) could be better.
    Yours could also always be better.

* **Be humble** - Realise that you can learn from everyone out there, including
    those are just learning to write code, and even from those who don't write
    code at all.

A good chunk of these have been taken from [OK GROW!'s development process][dev process]
guide, which I've contributed to a bit.

A lot of these may seem like common sense, and I hope that they do. That's a
sign that you've got solid guidelines in place. But I've had some encounters
with people who haven't given such things any consideration, just like there
are companies out there that still don't use source code control.

What sort of guidelines do you use in your development process? Email me at
rgould@u2622.ca or leave a comment below. I'd love to hear them!

[broken window]: https://blog.codinghorror.com/the-broken-window-theory/
[dev process]: https://github.com/okgrow/guides/blob/master/docs/Development-Principles.md
[software rot]: https://en.wikipedia.org/wiki/Software_rot
