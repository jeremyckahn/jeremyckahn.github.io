+++
title = 'Unkillable Apps'
date = 2023-11-05T16:42:22Z
draft = false
+++

Good software doesn't die. Great software _can't be taken away_.

Much like a [cool URI](https://www.w3.org/Provider/Style/URI), software is only relevant so long as it's available for use. Unfortunately, software is trending towards a fragile design: The Cloud. If you're a Cloud Architect and reading this, relax. This isn't a condemnation of your work. Cloud-based architecture has many benefits and there is a place for it. However, it is fundamentally flawed in a key way: The user doesn't own the software. At best the user _rents_ the software, and even then the user can be evicted ([or worse](https://www.nytimes.com/2022/08/21/technology/google-surveillance-toddler-photo.html)) with no recourse. This is a critical design flaw for many use cases and there needs to be an alternative.

We need software that doesn't go down when AWS does. We need software that the user owns and controls. We need software that can't be taken away due to [corporate whims](https://killedbygoogle.com/) or [government overreach](https://en.wikipedia.org/wiki/Censorship_of_GitHub). We need **Unkillable Apps**.

## Anatomy of an Unkillable App

An Unkillable App is:

- Open source
- A self-hostable static web app
- Cloud-agnostic

Let's dig into each of these characteristics.

### Open source

The foundation of an Unkillable App is its source code. If the user does not have access to their software's source code, then they have no ability to modify its operation. If your app is not open source, then it is trivially killable and you might as well stop reading this article now.

With open source code, the user is empowered to fix bugs and make updates when the software's context changes. For example, closed-source software is liable to be abandoned by its developer and may cease to function when the operating system it runs on is updated.

Open source software is automatically redundant. Everything on the internet is permanent ([for better or worse](https://www.normantranscript.com/news/once-on-the-internet-always-on-the-internet/article_4bb953b0-8804-11eb-9bad-c7b05bdeb4cc.html)), and that includes published source code. It is trivial to hit the Fork button in GitHub or simply `git clone` a project to preserve it offline. When software is open source, everyone owns it and it cannot be taken away. A hostile government could attempt to suppress an open source project ([and they do](https://element.io/blog/india-bans-flagship-client-for-the-matrix-network/)), but there are no technical means by which they could remove it from existence.

Open source software will last until the end of the internet.

### A self-hostable static web app

Open source software is a great place to start, but it won't do people much good if it can't actually be run. Software that's designed to be [self-hosted](<https://en.wikipedia.org/wiki/Self-hosting_(web_services)>) is designed to survive. This doesn't mean that software _must_ be self-hosted (after all, doing so is extra work), but it must be available as an option in case the principal version of an app becomes unavailable. Think of it as a [failover](https://en.wikipedia.org/wiki/Failover) mechanism. To make self-hosting practical, complete application data export functionality must be available to users so that they can migrate between app instances.

Software that is open source and self-hostable is a [hydra](https://en.wikipedia.org/wiki/Lernaean_Hydra). You can try to kill it, but it will always reappear elsewhere.

The simplest kind of app to self-host is a [static web app](https://www.staticapps.org/articles/defining-static-web-apps/). It's strictly a set of HTML, CSS, and JavaScript files. If built appropriately, it will run on any device. A static web app is immune to operating system updates and the risks of outdated system libraries. And web apps can last **forever.** The original [Space Jam website](https://www.spacejam.com/1996/) is still online and functional because it was built to web standards. Web standards are both stable (once completed) and [powerful](https://whatwebcando.today/).

I've written previously about [the incredible power of PWAs](https://jeremyckahn.github.io/posts/pwa-agony-and-ecstasy/). That power can be made available indefinitely if it is built to be self-hosted and not reliant on specific cloud services.

### Cloud-agnostic

A static web app can be served from any HTTP server. That flexibility lends a lot of durability because anyone can run an HTTP server. Why not extend that flexibility to any web services that the app depends on?

It would be very limiting to artificially restrict a web app to just locally-available APIs. After all, web browsers are most powerful when they connect to other computers and exchange data. Unkillable Apps don't depend on proprietary web services. Instead, they treat web services like a "dumb" resource. A practical example of this is remote data storage. Rather than building a web app's storage mechanism around something like AWS S3, consider building it to use generic file storage solutions as a back end. You could integrate with [Nextcloud](https://nextcloud.com/), Dropbox, Google Drive, etc. and allow the user to log in to whichever storage provider they want. [StackEdit](https://stackedit.io/) is a shining example of this. StackEdit persists data locally by default but offers the option to sync with Dropbox, Google Drive, GitHub, or GitLab. Even if the developer of StackEdit abandons the project, I can be confident that I'll always have access to my data because it was stored in the system of my choosing.

An Unkillable App relegates the cloud to being an implementation detail. When one doesn't meet the needs of the user, they can trivially switch to one that does.

## Unkillable apps for a better future

I believe the future of software can be bright and amazing, but only if we design for it. We have to choose open source. We have to choose a standard and stable technology platform. We have to choose to be cloud-agnostic. **We have to choose to build software that cannot die or be taken away.**

Users need to rightly trust that the apps they depend on will be there tomorrow. Because if we don't do this, we will always be dependent on corporations that do not prioritize our interests.

We have the tools to build the future we want. So let's build it!
