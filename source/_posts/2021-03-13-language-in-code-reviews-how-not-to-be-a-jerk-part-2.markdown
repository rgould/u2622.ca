---
layout: post
title: "Language in Code Reviews: How not to be a Jerk, Part 2"
date: 2021-03-13 16:52:25 +0100
comments: true
categories: 
---

[Part 1]({% post_url 2021-03-13-language-in-code-reviews-how-not-to-be-a-jerk-part-1 %}) \| Part 2

“Man, your code reviews are brutal!” says John to your teammates. He’s talking about you.

“Why do you hate me so much?” writes Steve in an email to you.

Sound familiar? You might just be Seth, one of the people most familiar with the project and gatekeeper of the code base. You’re not out to write “brutal” reviews, or make your colleagues hate you. You just want to ensure that only the highest quality code makes it into production, as bug free as possible.

So why do your coworkers think you hate them? When you write things like:

> can’t you just do it this other way?

> kill this

> you can’t do that

They really hear:

> “only an idiot would do it this way”

> “why would you commit this?”

> “aren’t you smart enough to realise that that won’t work?”

But that’s not really how you intended to come off, or you likely wouldn’t be reading this.

To try to understand more of John and Steves’ perspectives, read [Part 1]({% post_url 2021-03-13-language-in-code-reviews-how-not-to-be-a-jerk-part-1 %}) of this article.

So why should you even care? Can’t John and Steve just grow a thick skin? Why can’t they just stop whining?

Because they’re human, and we all have extremely varying experiences, all of which drive how we interpret the behaviour of others. Some people will assign a benevolent tone, while others will just as easily assign a malevolent one.

When John and Steve interpret your comments negatively, their performance will decline. They will feel like shit, their productivity will drop, and they will resent working with you. They will not be able to thrive in such an environment, and your overall team performance will suffer.

Fortunately, you can fix it. And when you do, your teammates will think more highly of you, enjoy working with you more, and be friendlier to you. Their morale will increase, and their productivity with it.

It all starts with having the right tone. Without proper use of tone, it’s very easy to to lose the meaning behind the message.

When tone isn’t explicit, it’s easy to interpret it negatively. It’s also highly individual: John may read a comment as a friendly suggestion, while Steve reads it as an attack on his intelligence.

Writing comments without paying attention to tone is a default mode for most people. You must consciously insert tone when writing in order to prevent John and Steve from attributing a negative tone.

Fortunately, it’s a lot easier to fix than you would think. With some practice it will become more natural, and eventually you will be inserting explicit tone automatically.

<img src="/images/hntbaj2-1.jpg">

The following techniques aren’t just applicable to just code reviews, but to all text-based communication you’ll use in daily life: emails, texting, chat, etc. Follow these suggestions and John and Steve will no longer think of you as a brutal gatekeeper:

## 1. You must focus on making your tone friendlier.

You can use the passive voice to remove a subject from the sentence, placing emphasis on the outcome of the action. This focuses on the problem, and not the person. Instead of “You must use four spaces for indentation”, use “Four spaces must be used for indentation.” Notice how the “you” has been completely removed from the sentence.

Example

 * Bad: Kill this.
 * Good: Er, was this accidentally committed?

You can also use the collective “we” in place of “you”. For example, instead of “You must always re-throw exceptions here”, use “We must always re-throw exceptions here.” This de-emphasizes the original submitter as the target of the comment, and re-emphasizes that this is a team effort.

Example

 * Bad: Can’t you just do it this other way?
 * Good: Unfortunately we need to it this particular way, or else the whizbob will become unstable and raise exceptions.

Use the passive voice, the collective “we”, and focus on the problem, not the person.

## 2. Ask questions.

Asking questions is also a great way to bring up an issue. They become responsible for the answer, and this gives them a chance to explain themselves. For example: Instead of “this will fail”, try “What happens if the gidget is set to 42?” It could be that they have a legitimate reason for submitting the code as it is.

Example

 * Bad: You can’t do that.
 * Good: Are you sure that this is going to work? What happens if chunky_bacon is set to null?

## 3. Build good rapport with your teammates and they will integrate that into your tone.

Additionally, build rapport with the submitter. Eat lunch with them, play games with them (in person or online), get to know them. If this is something that is difficult for you, begin with a casual “got any plans for the weekend?” Show some interest in their response. If they answer with “I did some karate”, ask them about it. “Oh cool! How long have you been doing karate for? What do you enjoy about it?” Keep the questions focused on them, and don’t bring the conversation back to you. Bad example: “Oh cool! I’ve always wanted to do karate.” This brings the conversation back to you, and gives them the opportunity to lose interest.

## Additional strategies you can use:

**Avoid imperative forms.** Make suggestions, not commands. Instead of “do it this way”, try “it might work better if we did it this way.” If you issue commands you will come across as demanding.

**Prefer an informal tone over a formal tone.** Instead of “This could be null here.”, try “this could be null here”, noting the lack of punctuation. Punctuation is still important, but the use of initial capitals and final periods can be safely discarded.

**Don’t end your statements with a period.** Studies have shown that ending your sentences with a period makes them come across as less sincere.

**Use liberal use of emoticons and emoji.** They explicitly demonstrate tone :) If you’re worried that the receiver will be annoyed by them, pay attention to how they themselves write, and tailor your level of emoticons to match theirs.

**Don’t be terse.** Terseness comes across as impatient and frustrated. Instead of “don’t do this”, prefer “if we do it this way, these bad things could happen”, or even better: “can you foresee any bad things happening if we do it this way?”

**Admit that you may not understand everything.** Instead of “don’t do this”, try “I don’t understand this. Would you be able to elaborate?”

**Have clear guidelines and coding styles so that they don’t turn into an issue during reviews.** Have an automated tool to check those styles before code is even committed.

**Make it explicit when a comment is a suggestion**: “it might work better if this implementation had rockets”.

**Make it explicit when a comment is a mandatory change**: “unfortunately we must transmit the the signal here, or the aliens will die”

**Add compliments, acknowledgement, and gratitude**: “Thanks, this looks awesome! Just a few things that I think we should change.”

**Don’t write in anger.** If you find yourself thinking “how the fuck did this get written?” Take a deep breath, step away from the computer for a few minutes. Calm down, come back, and write “I’m not sure this will run without throwing an error.” Otherwise you risk building resentment in the receiver.

<img src="/images/hntbaj2-2.jpg">

Still worried that your colleagues might be interpreting your comments negatively? Grab them and go over your code review together, whether it’s in person or using Screenhero. Then you can explicitly add your tone in your voice.

With these guidelines, you’ll start to find that John and Steve are friendlier towards you, and their productivity will increase. These techniques will help you across all written communication, not just for code reviews. You will become a more pleasant person to work with, and that alone makes it worth the effort.
