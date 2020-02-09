---
layout: post
title: "Git command customizing"
date: 2020-02-09 21:50:00 +0900
categories: tech
---
# How to customize git command in bash?
I wanted a shorter commands and default actions.

for example:
> `co` -> `git checkout master`
>
>`co -t develop` -> `git checkout -t develop`

Add this code to your .bashrc(Linux) or .bash_profile(MacOS)
``` bash
export DEFAULT_BRANCH='master'
function co() {
        if [ $# == 0 ]; then git checkout $DEFAULT_BRANCH;
        else git checkout $*; fi
}
```

### *Finsh!*

[yungik]: https://yungik.github.io/
