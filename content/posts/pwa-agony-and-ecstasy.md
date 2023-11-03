+++
title = 'The Agony and Ecstasy of PWAs'
date = 2023-11-03T13:48:42Z
draft = false
+++

I love [PWA technology](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps). I think it's the most powerful and empowering technology that has come along since the creation of the internet. And it's never going to succeed.

Why is this? How could a great technology utterly fail to make meaningful market share inroads? Let's explore why PWAs are awesome, and why nobody cares.

## User-centric design

Progressive Web Apps (PWAs) are literally just web pages with some additional functionality to make them behave like a native application. The key components of this illusion are the ability to install the web page such that it appears alongside actually-native apps like Microsoft Paint or Apple Messages, and some level of offline functionality. When opened, PWAs render in a dedicated window as their own app, distinct from any browser. Under the hood they're just another browser tab, but they present as a fully-formed, installed application.

Because PWAs are web pages at their core, they natively offer all of the benefits of a standard web page. That includes [accessibility](https://developer.mozilla.org/en-US/docs/Web/Accessibility), [security sandboxing](https://wiki.mozilla.org/Security/Sandbox#Overview), the potential to be customized via browser extensions, and observability via browser devtools. Every mainstream web browser has devtools that allow the user to take a look at the code that's running on their device. Most people won't do this, but the important thing is that they _can_. Observability is a de facto right of web users that cannot be taken away by web developers[^1]. And this is wonderful. I can't think of any other mainstream technology platform that puts the user's interests ahead of the developer's in this way. Because of this, PWAs are inherently user-centric in a manner that native apps uniformly choose not to be.

[^1]: It's worth mentioning that developers can (and generally should, for performance reasons) minify their code before deploying it. This makes it less than trivial to figure out what the code is doing, but the point is that it's possible to do so, rather than impossible (or [harder](https://www.nowsecure.com/blog/2021/09/08/basics-of-reverse-engineering-ios-mobile-apps/), anyways) like it is with native apps.

In general the tech industry has sort of lost the plot of what we're trying to accomplish. Computers are magical and amazing things, and they could do so much great stuff for people. Unfortunately "tech" has been largely co-opted by VCs into being a wealth extraction mechanism, so user-centric design has taken a back seat to investor-centric design. This has led to widespread [enshittification](https://en.wikipedia.org/wiki/Enshittification) and a general degradation of product quality. I don't see this changing in the near future, but the user-centric design built in at the platform level of PWAs at least gives us a hope that it someday could.

## Simple deployment

Not only do PWAs offer the most user-centric design, but they have the most developer-centric deployment mechanism available as well: The web! Depending on how a project is set up, deployment could be as simple as modifying a file on a server. By contrast: If you want to update a native app, you need to submit your change to the app store operator (Apple, Google, etc.), wait, and pray that they accept it. Native app developers have no real control over the software that is delivered to their users because app store operators could capriciously deny updates for any reason. _They_ own the deployment platform.

With web technology, the server is the deployment platform. You could run one for free from home, if you'd like. The web also has no gatekeepers or censors. There is no inherent payment processor that skims 30% off of every transaction. The web lets you own and control the code, the infrastructure, and the content. And the best part? PWAs run on every device! There's only one build target. It is the most successful implementation of "[write once, run everywhere](https://en.wikipedia.org/wiki/Write_once,_run_anywhere)" in history. I struggle to conceive of a better way to ship software.

So far I've extolled the myriad virtues of PWAs and you're hopefully as excited about them as I am. If you are, prepare to be disappointed!

PWAs have struggled to gain meaningful app market share, and I don't expect that to ever really change. There are two main reasons for this: Gatekeeping incumbents, and user expectations.

## Corporate incentives stand in the way

Apple effectively invented the concept of a modern app store, and it makes them billions of dollars a year. Many people seem to consider their practices unfair. I don't quite see it that way (nobody is requiring developers to publish with Apple), but I do see what such a market position means for us. iOS and its derivatives offer only one web browser[^2], Safari. The problem is that Safari has always lagged behind the other major browsers in its feature set. This holds iOS back, and it therefore holds the potential for PWAs back as well because it's such a major platform. After all, why would a developer invest resources into a project if it won't work properly on [over a quarter of mobile devices](https://www.statista.com/statistics/272698/global-market-share-held-by-mobile-operating-systems-since-2009/)?

[^2]: Yes, I know there's other browsers on the iOS App Store. But due to Apple's restrictions, they're implemented as reskins of Safari and therefore cannot implement the web platform features that Safari is missing.

Apple has an obvious incentive to limit its browser's capabilities: Apple can't monetize the web. Being the cunning profit-driven corporation that it is, Apple is going to seek to widen its various [moats](https://www.investopedia.com/ask/answers/05/economicmoat.asp) as much as possible. Why invest in a technology that doesn't produce revenue when you could invest in one that does? It's hard to fault their logic, but the end result hurts users because it disincentivizes developers from creating PWAs and therefore diminishes user freedom.

## User expectations

PWAs, as a concept, don't make sense to the average person. PWA installation is effectively a power user feature because typical users don't even consider the concept. Computer users have been implicitly trained for decades to think of web browsers as a means of basic content access and to rely on installed native apps for more advanced work and engagement. Can you honestly think of anyone in your life (who isn't a web developer or technology enthusiast) that would default to installing an app via the web rather than their app store?

This isn't actually a technology or design problem. No, it's a _marketing_ problem. Marketing problems can only be solved with money, and there isn't a clear ROI in solving this particular one. So things will likely remain this way.

"We just need an app store for PWAs!" I hear you say. Bad news: It's been tried and it hasn't succeeded. [Appscope](https://appsco.pe/) has been abandoned and nobody is talking about [store.app](https://store.app/). I _want_ these stores to win. I just don't see the business model to support them, though.

I really want to be wrong. I want to see PWAs flourish and render native apps irrelevant. But there needs to be a killer business model behind them for it to happen. Without that, the primary audience for PWAs is other web developers.

## What we can do

The good news is that PWAs aren't going anywhere. It's a web standard that's in wide deployment. It's an effective technology choice for hobby projects and side hustles. I don't see Apple ceding its market share any time soon, but that doesn't mean that we can't enjoy PWAs today and into the future. I think **we just have to accept that it will always be a less successful platform, especially for Apple users**.

I plan to keep making open source PWAs because it's such an effective solution for [the hobby projects I like to build](https://github.com/jeremyckahn/). I encourage you to do the same. If you value developer control and user freedom, PWAs are the obvious choice.
