---
author: Clau Batista
title: Patch stacks
date: 2022-01-15
description: A introduction about my Outreachy internship
tags: [outreachy, internship, devtools, firefox]
series:
  - series-outreachy
---

hello folks 🤙🏼

When Outreachy suggested that we write about an open source vocabulary term, I was very confused and lost, not knowing what I would write 🙃. A “vocabulary term” could be a word, phrase, acronym, or concept that was new to us.

After two Outreachy tries and some time contributing to Mozilla, I feel a lot more familiar with the terms and the tools. Obviously, it wasn't always like this, Mozilla has a particular process, some projects use GitHub to file the issues, but Mozilla also has Bugzilla, which is a website to track bugs. There are also, Phabricator, and Searchfox (which is my best friend now).

When I started my internship, I was familiar with these tools. However, in my time contributing, I worked on isolated bugs mostly from unrelated projects, so I could work in one bug, finish it and only then start a new one. On my first week I was a bit disoriented, because my bugs depended on each other and I had a deadline, so I couldn’t just wait for a bug to be merged to start the next. I asked my mentor the best practice here, and he told me I could work on top of my first bug, before it was landed 🤯.

I was learning about **patch stacks.**

![https://media.giphy.com/media/xUPGckDoXF37BtZMUE/giphy.gif](https://media.giphy.com/media/xUPGckDoXF37BtZMUE/giphy.gif)

Patch stacks are a group of patches that depend on each other. This allows to break patches in small pieces, which are easier to review, and allow you to work faster.

Patch stacks are analogous to GitHub pull requests with multiple commits. However, patch stacks go beyond pull requests. On Phabricator, each commit results in a separate patch, because each commit is a separate patch, they can also be reviewed, accepted and landed separately. This makes it easy for me to move on to new bugs before a previous blocking patch is landed by adding new patches to my stack. In GitHub, if I kept adding new commits to an existing pull request, that would just delay merging and make reviews harder. See, for example, the current patch stack I’m working on:

![Sreenshort about my stack](/images/01-15-2022-patch-stack.png)

I’ve been using this [source](https://firefox-source-docs.mozilla.org/contributing/stack_quickref.html#rebasing-the-stack) to help me, and of course I ask questions. Sometimes I forget that it is ok to ask questions, because I don’t want my mentor to know that I don’t understand something, but a note to myself: **it is TOTALLY ok to not know.**

Thanks for reading, I hope you can enjoy the next ones too.
