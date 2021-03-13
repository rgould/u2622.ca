---
layout: post
title: "Language in Code Reviews: How not to be a Jerk, Part 1"
date: 2021-03-13 16:51:29 +0100
comments: true
categories: 
---

Part 1 \| [Part 2]({% post_url 2021-03-13-language-in-code-reviews-how-not-to-be-a-jerk-part-2 %})

<img src="/images/hntbaj1-1.jpg">

“Jerk”, “Asshole”, “Ugh, what now?”, “Do it yourself!”, “Why are you so damned picky?”

Sound like things you’ve thought to yourself when Seth submits his review for your most recent pull request? Seth is the rockstar, know-it-all, pretentious, two-spaces-not-four and definitely-no-tabs-ever guy. He’s the gate-keeper of all code. He reviews all pull requests, and nothing gets into the code base without his approval. It’s his fault that you can’t meet your deadlines. Why can’t he just approve it so that you can move on to the next task?

Well, he could. But there are some very good reasons he wouldn’t want to.

It turns out that Seth probably isn’t as bad of a guy as you would think. The reason you feel this way could be aggravated by the tone, or more importantly, the lack of tone that was used in his comments while reviewing your code. That his comments made you feel shitty are a combination of multiple factors:

 * the tone (or lack of tone) Seth used
 * how well you know Seth
 * your rapport with Seth
 * your mood and energy levels when reading the comments
 * Seth’s mood and energy levels when writing the comments

All of these factors can combine to ruin the relationship you have with Seth. They can also turn your this-should-be-awesome day, into fuck-this-get-me-out-of-here day, where you struggle to crawl out of bed the next day, just to plop yourself in front of the computer, only to re-read the comments and spiral back into that foul and depressive mood again.

<img src="/images/hntbaj1-2.jpg">

But there is a way out: Seth isn’t actually an asshole — it just seems that way due to how you’re interpreting his comments. Seth really just wants to make sure that the code that makes it into production doesn’t introduce any bugs.

Are you Seth? Then I recommend you read [Part 2]({% post_url 2021-03-13-language-in-code-reviews-how-not-to-be-a-jerk-part-2 %}). For now, we’ll talk about how it is to be the receiver of Seth’s comments.

Tuesday morning. Opening Gmail, you see a thread containing comments from the pull request you submitted yesterday. It’s from Seth, of course. You grit your teeth, wondering if you should put your mouthguard back in. At this rate, your molars will be ground down by the time you hit forty. Tensing your muscles, you open the thread.

>   kill this

>   this must be a typo.

>   this does not look good to me. Why was this done?

Yup, sounds like Seth is his normal, moody self. But wait, there’s more:

>   can you not just change it so that it uses attributes?

>   why can’t you just do it this way?

>   can you explain this change?

And you’ve got your daily standup in ten minutes! Now you’re thinking that it might just be best to call in sick and play video games all day.

Does this sound like you? Even just a little bit? Read on. Even if it doesn’t sound like you, you may run into this in the future, so you may want to keep these things in mind.

It’s very easy to see Seth blaming you for this. “Can you not just do this?” “You must surround function parenthesis with spaces”. It’s all your fault, and Seth is making sure that you remember that.

Well, not really. There could be an entirely different side of this story: Seth is in a rush, and only has a few minutes to conduct your code review, one of many that he has to get done every day. It shouldn’t come as a surprise that his comments are terse, such as “remove this”. Seth doesn’t really hate you at all, he just wants to get the code review over with so he can go on to fix the issue that brought the database down last week.

<img src="/images/hntbaj1-3.jpg">

How did this conspire to ruin your day in the first place?

Well, Seth’s comments lack tone. When they lack tone, it’s very easy to insert a tone that matches your current mood, or one that reflects how you think Seth feels about you. If you think Seth hates you, you will interpret it in that tone. If you’re feeling down or frustrated, Seth’s comments will seem like he is frustrated too. And after you hear those tones once, you’ll likely interpret his future comments in similar tones.

“That’s great, but what can I do about it?” you ask.

Well, it turns out that you can change how you interpret such messages. In Learned Optimism, Martin Seligman writes about a technique that people can use to help stop interpreting comments as personal, general, and permanent, and interpreting them as impersonal, specific, and temporary. Reginald Braithwaite gives a much better overview here. Go read it.

[Optimism](http://braythwayt.com/homoiconic/2009/05/01/optimism.html)

You can learn to read such comments in a more positive, friendly tone, but it also helps to build a good rapport with your reviewers. If you haven’t met them in person yet, make it a priority to to do, if possible. Once you get to know someone in person, it becomes a lot easier for you to transfer their in-person personality to their tone-less comments.

If it’s not feasible to meet them in person, try to organise things you can do together online. Play some games online together, with microphones on, or have a “happy hour” for the team, where everyone jumps on hangouts and has a virtual drink together.

Also if you’re comfortable with it, the best course of action may be to try to talk to Seth directly. Don’t open with a bold statement like “Why do you hate me?” That implies that Seth actually does hate you, when it’s likely far from the truth. Try something like this: “When you do X, I feel Y, and that makes me Z”. Following that formula focuses on your feelings and the impact it’s having on you, rather than attacking Seth. Try it out: “When you say ‘kill this’, that makes me feel like you’re frustrated with me, and that makes it more difficult for me to come into the office.”

If that sounds really daunting to you, or you don’t feel comfortable enough with Seth to talk to him like that, you may try an indirect approach. Post the second part of this article in your team’s chat, suggesting that everyone read it. When Seth comments on another team member’s pull request, point out to him how negatively his comment can be read, and encourage him to add explicit tone to his posts.

The key take away here is that you don’t want to attack Seth; That will only make things worse. Focus on how it feels to be on the receiving end of those comments, and Seth will be able to show a bit more empathy. Encourage, don’t disparage.

You may also feel shame that Seth is pointing out something that you know you could have done better, but you have to take it into context: You may not consider it to be your best work, but it was the best effort you could give at that time. If you’re under pressure, in a time crunch, working overtime, distracted, sick, or otherwise exhausted, you’re not going to be able to do your best work. In this situation, it’s best to view it as a chance to improve something that you did before, and to know that the next time you do something like that, it will be caught by Seth. It’s also a chance for you to be grateful that such code did not make it into production.

<img src="/images/hntbaj1-4.jpg">

How can you continue to work with Seth? In summary, here is how you can make it more enjoyable:

 * Build rapport: spend time in other fun activities; meeting in person; if remote, play games or hangout online
 * Learn how to control how you read tones in messages (helpful even beyond this scope)
 * Empathise with Seth: he wants the code to be bug free
 * Communicate: talk to Seth about the tone in his comments

As a reviewer, Seth has a hand in it as well. He can spend just a little bit of effort to add some tone to his comments. In [part two]({% post_url 2021-03-13-language-in-code-reviews-how-not-to-be-a-jerk-part-2 %}), learn how to not be a jerk when doing a code review.
