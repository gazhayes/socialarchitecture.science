---
title: Contributors SHALL NOT have commit access to the repository unless they are
  also Maintainers
date: 2018-04-09 00:00:00 +0000
---
Rule 2.1.7 of the C4 states that:

**_Contributors SHALL NOT have commit access to the repository unless they are also Maintainers._**

As [this issue](https://github.com/isaacs/github/issues/153) from 4 years ago states, contributors to a repository cannot self-assign issues or apply labels to issues unless they have full commit access to the repository.

My first thought was "_this is stupid, let's just fork github itself and put it under the C4 so that developers actually get the platform they want_". Guess you have to pick your battles though.

So instead, we started violating the C4 and giving everyone write access. The problem is that when you have 20 contributors to a fast moving project, people don't want to open each individual issue and read through the conversation to see if someone has said "hey I'm gonna work on this one". So instead, contributors can self-assign issues and then everyone else knows not to try and solve that problem.

It was going alright for a while, but as not everyone understands the C4 (it takes a while for the Soviet mind to stop clinging to the artificial stability of the centrally planned economy and embrace the fee market). So we ended up having problems like this:

![](/uploads/2018/04/09/Screen Shot 2018-04-09 at 4.24.41 PM.png)

This was a _correct patch_ under the C4 that was closed by someone who isn't a maintainer and doesn't understand the philosophy behind the C4 protocol. To his credit, Janat08 did save something from breaking, but this should have been expressed through a patch and not by closing someone's pull request (or better yet, by writing a test that would have picked this up).

There have also been a few accidents - non-maintainers merging their own commits by accident. There's also the clear risk of someone accidentally pushing straight to the repo.

The reason for this rule in the C4 is that maintainers are only maintainers because they understand the protocol. Their role is to enforce the protocol, not make judgments about good/bad code. There's another rule in there too: 

**_A new Contributor who makes correct patches, who clearly understands the project goals, and the process SHOULD be invited to become a Maintainer._**

So it's not like there's a boys club of maintainers, a maintainer doesn't even need to know how to code. They just need to understand the process. 

The simplest solution to this problem appears to be to adopt the use of the  [Zulip bot](https://github.com/zulip/zulipbot). 

This bot allows _anyone_ to self-assign issues, and to apply labels to issues, by making comments and mentioning the bot.

This should theoretically solve these problems. Though I'm not sure how all the non-maintainers are going to react when I remove their write access. I'll update this post when I find out.