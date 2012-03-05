---
layout: post
title: "Screencast: Using Shell History to Create Aliases"
date: 2012-03-04 19:15
comments: true
categories:
---

Contents:

1. Introduction to aliases @ 0:00
1. Analysing shell history to create relevant aliases @ 4:43

Download: [mov](http://rgould.ca/downloads/aliases.mov) 24MB, 8:26 (Recommended)

Watch (recommended in full screen and in HD):

<iframe width="420" height="315" src="http://www.youtube.com/embed/e4bQ4FstNvs" frameborder="0" allowfullscreen></iframe>

Notes:

Make an alias:
``` bash
    alias l="ls -al"
    alias glog="git log"
```

Add those to your `~/.aliasrc`.

Modify `~/.zshrc` or `~/.bashrc` (works for both):
``` bash
    if [[ -r ~/.aliasrc ]]; then
      source ~/.aliasrc
    fi
```

View shell history: `history`

View count of common commands:
``` bash
    history | awk '{ print $2 }' | sort | uniq -c | sort -n
    history | awk '{ print $2,$3 }' | sort | uniq -c | sort -n
```
Use that output to create better aliases!

Here's some of my favourite aliases:
``` bash
    alias ..='cd ..'
    alias ...='cd ../..'
    alias ....='cd ../../../'
    alias .....='cd ../../../../'
    alias be='bundle exec'
    alias g=git
    alias ga='git add'
    alias gc='git commit -v'
    alias gca='git commit -v -a'
    alias gch='git checkout'
    alias gl='git pull'
    alias gst='git status'
    alias l='ls -al'
```
