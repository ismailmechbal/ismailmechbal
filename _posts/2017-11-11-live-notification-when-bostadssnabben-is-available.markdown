---
layout: post
title:  "Live notification when Bostadssnabben is available"
date:   2017-11-11 08:57:48 +0200
type: post
description: A tool that notifies you whenever a new appartment is available through Bostadssnabben
image: https://bostad.stockholm.se/globalassets/generella-bilder/600/600-gaende-med-mobil.jpg
---

Sweden housing crisis is becoming an international discussion, BBC wrote an interesting article [The city with 20-year waiting lists for rental homes](http://www.bbc.com/capital/story/20160517-this-is-one-city-where-youll-never-find-a-home).

As a matter of fact, you’ll need to sign up your child to this list as soon as he is born to ensure he can get a flat when he reaches his 20’s.

[The local](https://www.thelocal.se/20170828/the-story-of-swedens-housing-crisis), wrote an interesting article with some scary numbers: "For an idea of just how long those queues can be, in the Swedish capital, the number of people waiting to rent an apartment from Stockholm's Housing Agency (Bostadsförmedlingen) grew by almost 40,000 last year – and there are now almost 580,000 waiting to find an apartment through that method (although not everyone in the queue is necessarily actively apartment-hunting).
During the same year only 6,900 new apartment rentals were brokered by the agency. At that pace, it would take half a century for all of the people on the waiting list to earn a standard long-term contract."

However, there is a fast track, Bostadssnabben, where the principle is based on first in first out or in other words if you’re the first to apply then the flat is yours, if requirements are met.

I wanted to see if there is any way to automate this task, at least the first part, getting a notification when a new fast track flat is available, thankfully there is a public endpoint that can serve us.
[https://bostad.stockholm.se/Lista/AllaAnnonser](https://bostad.stockholm.se/Lista/AllaAnnonser)

I wrote a small Ruby script that request this endpoint every 5 minutes, 5 times a day from Monday to Friday between 7am and 6pm. The script search for the value of Bostadssnabben: True and if found will post to my Slack.

[https://github.com/ismailmechbal/bostadssnabben](https://github.com/ismailmechbal/bostadssnabben)

It has been 3 weeks now since the script is deployed and no fast track has been submitted yet!