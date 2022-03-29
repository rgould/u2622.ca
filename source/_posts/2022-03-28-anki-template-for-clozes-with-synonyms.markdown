---
layout: post
title: "Anki Template for Clozes with Synonyms"
date: 2022-03-28 21:42:05 +0200
comments: true
categories:
---

If you use a cloze-style (aka. fill in the blank) question when learning vocabulary, you eventually come across a synonym. For example in German, you have _wohnen_ and _leben_, and they mostly mean the _to live_. You can put it in the card as superscript:

Front: Wo \[\[live]]<sup>lebst</sup> du?<br/>
Back: wohnst

<img src="/images/anki_synonym_example1.png" width="50%" alight="right">

There are a couple problems with this approach.

First, it's a bit unnatural to type. Would you rather type "Wo wohnst du?", or "Wo live du?".

Second, it doesn't work well if you want to generate text-to-speech (TTS) audio samples en masse with [AwesomeTTS](https://ankiweb.net/shared/info/1436550454). If you pass this card to AwesomeTTS, it will generate audio with input "Wo \[\[ live ]]lebst du?", which generates nonsense. What you want to feed it is: "Wo wohnst du?"

<img src="/images/anki_synonym_awesome_tts1.png">

What if we use the built-in cloze template? Then the card would look like this:

Text: Wo \{\{c1::wohnst::live}}<sup>lebst</sup> du?

<img src="/images/anki_synonym_example2.png" width="75%">

This is a bit more natural to type (start with "Wo wohnst du?" then add the cloze, then add the synonym). Anki has shortcuts for adding a cloze (⌘-C / ALT-C) and for adding superscript (⌘-SHIFT-= / ALT-SHIFT-=), making this a bit easier to type.

But this doesn't solve the second problem. If we feed this to AwesomeTTS, it will generate audio for "Wo wohnstlbest du?" which is still nonsense.

My solution: **Put synonyms in another field**.

Text: Wo \{\{c1::wohnst::live}} du?<br/>
Synonyms: lebst

<img src="/images/anki_synonym_example3.png" width="75%">

This is the easiest to work with, IMO. Once you add the cloze hint, you can hit TAB and then type out the synonyms. Also the Text field can be fed directly to AwesomeTTS and it will work as expected.

We can modify the template to show the synonyms following the cloze entry, so it looks exactly like it did before.

Here's the front:


```html
{{ "{{cloze:Text"}}}}
<br/>
<br/>
<span id="synonyms"><sup>{{ "{{Synonyms"}}}}</sup></span>

<script>
  var synonyms = $("#synonyms")
  synonyms.insertAfter($(".cloze"))
</script>
```

And the back is almost identical, just include the extra note:

```html
{{ "{{cloze:Text"}}}}
<br><br>
<span id="synonyms"><sup>{{ "{{Synonyms"}}}}</sup></span>

<script>
  var synonyms = $("#synonyms")
  synonyms.insertAfter($(".cloze"))
</script>
<hr>
{{ "{{Back Extra"}}}}
```

Voilà!

<img src="/images/anki_synonym_example4.png">

I've created a [sample deck](/assets/cloze-synonym-example.apkg) that contains the above template and note.

The original idea for this was provided by [Vocabulary Labs](https://vocabularylabs.com/) course, which I highly recommend!
