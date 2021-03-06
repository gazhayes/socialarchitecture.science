---
title: Introducing the C4 to existing projects
date: 2018-05-04 00:00:00 +0000
---
Let's do a thought experiment. Jump into your imaginary time machine and head on over to the year 2000.

You're tasked with ensuring Encyclopaedia Britannica's dominance over Wikipedia, by _becoming_ Wikipedia.

There's still a year before Jimmy Wales and Larry Sanger are set to register wikipedia.org, and Britannica has substantial resources and a huge market share. They even have a brand name that's endured since 1768.

How could you possibly fail when you have Britannica's resources combined with that robust foresight only time travel can provide. Success is guaranteed.

The only thing you need to do is explain to the CEO of Encyclopaedia Britannica that the way forward is to fire all the contributors (including 110 Nobel prize winners, 5 former US presidents, and 4000 expert contributors) and simply let _anyone_ edit Encyclopedia Britannica. No experts needed.

***

You'll have just as much trouble _today_ trying to convince the gatekeepers of existing open source projects - especially cryptocurrencies - to adopt a software development equivalent of the Wikipedia model. Let _anyone_ edit the code? No way!

This is not a surprising situation, and it's unfair to criticise people for not entering the unknown. Adopting the Wikipedia model in an existing project is practically impossible because a leap of faith is required - only someone who's really experienced this approach first hand in one of their projects is capable of believing it can work. A leap of faith is required the first time, so it can only realistically happen when you start a new project that you don't really care about. As soon as you have something to lose, you can no longer experiment with the very foundation of the project. This is how many open source projects become victims of their own success, it becomes impossible to scale the developer community when you need "trusted" people to review every line of code before you merge it.

***

Monero is one of my favourite cryptocurrencies. The  environment that Monero is being developed in is the closest I've found to the Wikipedia model, which is why I personally value it far higher than the market does. It's the most friendly and open of all cryptocurrency communities. Monero is the absolute _closest_ that _any_ cryptocurrency has come to using the Wikipedia model - and yet it's a not even in the same galaxy.

Understanding why this is the case isn't difficult. Imagine you're a 'gatekeeper' at Monero and you want to introduce the C4 contribution protocol (the Wikipedia model of the software development world). There are _serious_ consequences for rocking the boat and messing things up. Things are working very well right now. Brilliant research is getting done. They are pushing the envelope in terms of privacy and security. They are coming up with quite genius solutions to blockchain bloat. Things really are working remarkably well. Would _you_ try and (truly) adopt the C4 in their position and let _anyone_ edit the code? It's easy to point fingers when it's not your head on the chopping board. I'd much rather be the CEO who sinks a large company than the vocal developer who's calls to adopt the C4 sink a cryptocurrency. 

With so many people having their money involved, the personal consequences for the developers, should they be deemed responsible for anything going wrong, would be disastrous. People would be out for blood.

This extreme example highlights why the C4 must be introduced at the _start_ of a project when there are no risks on the table and before people start forming a culture and expectations based on centrally planned processes.

## Fork the project

As it's practically impossible to convert an existing culture to the C4, the simplest solution is to implement the C4 on a new fork of the project. That way, anyone who likes the idea can opt-in and those who don't like the idea are not affected.

It's really quite simple: fork the repository, and change the contribution policy to the C4. You'll need at least one other person to be involved because you shouldn't be merging your own pull requests (or pushing code directly to the repository).

To make it easier, you might want to write up some basic instructions in the Readme on how to send a pull request and what it should look like.

Then you need to start following the C4 yourself, to the letter. You will be the example that everyone else initially follows, your actions will be reproduced by other people and be the basis for the culture of the project. If you set off on the wrong foot, you might find yourself unable to correct the culture and be forced to fork the project again.

### Housekeeping

There are usually a number of changes you need to make to a repository to start effectively using the C4.

### 1. Distribute the copyrights

Most open source projects centralize the copyright protections (e.g. _copyright \[project name\]_). All contributors thus implicitly (or even explicitly in many cases) surrender all rights to their code the very second they send a pull request. This makes it a trivial exercise to buy the copyrights, fork the project, change the license unilaterally, and move off in a closed direction.

This is why the C4 demands that copyrights be _decentralized_. The copyrights of C4 projects are owned by everyone who's ever submitted a line of code to the project, and you need the explicit approval of _all_ of them to be able to conduct any kind of takeover. This is practically impossible.

**How to do it:** add an AUTHORS file to the C4 fork of the project. Add your name, along with whatever the existing copyright notice is. The C4 asks that new contributors add their name to this file with their first pull request to the project. Over time, the list will grow.

### 2. Relicense as share-alike

Owning the copyrights to your code is useless if you're just going to turn around and explicitly hand over the rights on how your code can be used or licensed. If you release your code under a BSD/MIT style license then people or companies using your code are under no obligations to share their improvements with you, in fact it's trivial to make it illegal for you to use anything they develop on top of your code.

It seems rather silly to write code, then invite people to fork it for use in a closed source product that directly competes with your own work. It seems even more absurd to announce that you are happy to be prohibited from using any of the improvements your competitor has made to your work.

The simplest solution to this problem is to to use a _share-alike license_ that enforces remixability. This works hand-in-hand with the distributed copyrights  above, making it practically impossible for this enforced remixability to be removed.

**How to do it:** if the project you are forking is licensed under a BSD/MIT style license, it's very straightforward to relicense it as GPL or MPL (which are share-alike licenses. Simply replace the existing LICENSE file in the project with the new license. In a new file (e.g. LEGACY_LICENSES) add the line "Parts of this project were released under the following license and copyright:" followed by the original MIT/BSD license and copyright notice.

Amend all file headers to remove the previous license and add a line stating that the file is copyright the contributors listed in the AUTHORS file and released under the MPL (or GPL) license found in the LICENSE file. Below this, add something like "_Parts of this file were released copyright <original copyright name> under the MIT license contained in LEGACY_LICENSES_"

### Q: Is it legal to do this to someone else's project?

A: Absolutely and unequivocally yes (for BSD/MIT style licenses). In addition, after doing this, it becomes illegal for the original project to use any of the improvements made to your fork as that would allow people to use your code in closed source projects and prevent you from using any of their improvements.

It's best to explain the situation to the original project's maintainers, and out of goodwill explain that you are happy to simply ignore _their_ project's violations (but no one else's). Most people are unaware of the vulnerabilities that an MIT style license brings to their project and will simply change to a share-alike license when made aware. If they decide to cause any trouble for you, contact Github or wherever the project is hosted and file a DMCA takedown notice for any _new_ lines of code taken from _your_ project. This is a clear-cut open and shut case of copyright violation and their legal team will remove the code (or the entire project) faster than you can boil asparagus.
