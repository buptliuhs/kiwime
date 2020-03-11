+++ 
draft = false
date = 2020-03-11T16:00:54+13:00
title = "Some Useful Aliases in ~/.bashrc_profile"
slug = "" 
tags = []
categories = []
thumbnail = "images/tn.png"
description = ""
+++
## Some Useful Aliases
```
alias grep='/usr/bin/grep -n'
alias ls='/bin/ls -FG'
alias ll='/bin/ls -lFG'
alias cp='/bin/cp -i'
alias mv='/bin/mv -i'
alias rm='/bin/rm -i'
alias rmf='/bin/rm -fr'
alias vic='vi ~/.bash_profile'
alias sou='. ~/.bash_profile'
alias j7='/usr/libexec/java_home -v 1.7.0_79'
alias j8='/usr/libexec/java_home -v 1.8.0_45'
alias cdp='cd ~/Projects/gentrack/platform'
alias gl='git log'
alias gs='git status'
alias gd='git diff'
alias gb='git branch'
alias gc='git checkout'
alias gr='git rebase'
alias grom='git fetch && git rebase origin/master'
alias gcs='git add . && git commit -m "squash"'
alias g2='git rebase -i HEAD~2'
alias g3='git rebase -i HEAD~3'
alias gurl='git config --get remote.origin.url'
```