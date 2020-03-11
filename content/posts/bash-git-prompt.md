+++
draft = false
date = 2020-03-11T21:58:53+13:00
title = "bash-git-prompt"
slug = ""
tags = []
categories = []
thumbnail = "images/tn.png"
description = ""
+++
## [bash-git-prompt](https://github.com/magicmonty/bash-git-prompt)

### Installation on Mac OS X

- Run `brew update`

- Run `brew install bash-git-prompt` for the last stable release or `brew install --HEAD bash-git-prompt` for the
   latest version directly from the repository

- Now you can source the file in your `~/.bash_profile` as follows:

```sh
if [ -f "$(brew --prefix)/opt/bash-git-prompt/share/gitprompt.sh" ]; then
  __GIT_PROMPT_DIR=$(brew --prefix)/opt/bash-git-prompt/share
  GIT_PROMPT_ONLY_IN_REPO=1
  source "$(brew --prefix)/opt/bash-git-prompt/share/gitprompt.sh"
fi
```
