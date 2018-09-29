---
layout: post
title: Restoring lost commits
date:  2018-09-23 06:57:48 +0200
type: post
description: What to do losing your commits after git reset --hard HEAD^
image: https://www.ismailmechbal.com/images/blog/2018/09/git-reset-hard.jpeg
---

You just did `git reset --hard HEAD^` and all your last commit went to trash.

Luckily we can still get them if you did not run git gc (git garbage collection to clean it up), but who really does :p.

git fsck --lost-found

git reflog

git merge *latest commit HASH*

Thank goodness!