+++
title = 'A Future of the Web'
date = 2024-07-28T01:48:26Z
draft = false
+++

One of my favorite things about technology is seeing how it evolves over time and how we adapt to the changes it brings. In the 90's, digital documents were largely stored locally on people's computers. This was delightfully simple, but if there was a hardware failure or software bug, the document was gone forever. In the 2000's, we got cloud-based applications like Google Docs. This automated away the burden of data redundancy. If the device you were working on got lost or broken, you could log into the cloud service on another device and carry on with your work. From a user experience perspective, this seems to be the way that things should be.

As cloud-based apps evolved, they were necessarily designed around the business models of their developers. And business models, at least in the tech industry, are often at odds with the interests of users[^1]. In the case of Google, the relationship between the service and user is predicated on surrendering stewardship of the user's digital identity and property to Google. This is problematic, as Google is neither benevolent nor trustworthy. There are numerous reports of people losing access to their Google accounts due to [misinterpreted misuse](https://9to5google.com/2022/08/22/google-locked-account-medical-photo-story/) or [bad luck](https://news.ycombinator.com/item?id=20835350). Losing something as depended upon as a Google account would be catastrophic for many people. And Google has little incentive to improve the situation, as they have no real accountability to users when admittedly rare cases like these happen. But do you want to be the one-in-a-million person that inadvertently triggers a spurious policy violation and lose your Google account? I certainly don't. All that's left is to either live in fear of Google, live in ignorance of the risk, or find a different solution entirely.

[^1]: I specifically mean "users" and not "customers", because many of Google's users are indeed [the product and not the customer](https://quoteinvestigator.com/2017/07/16/product/).

The core of what Google offers as a cloud solution is fundamentally good at a high level, but it can't be trusted because of the interests and track record of the company that operates it. There are safer alternatives such as [Proton Drive](https://proton.me/blog/docs-proton-drive) that prevent the service from accessing user data. However, users still need to identify themselves to the service and manage their account credentials lest they lose access forever. We need something that's as private as Proton, but simpler to manage.

---

People often talk about "the future" of a given technology or domain. The future of mobile devices, the future of design, etc. But this is such a limiting way to see it! "The" future implies there is only path to go down, but there are in fact many possible futures that can happily coexist. The world is too complex for one solution to solve every problem well. There's space for more than one way of doing things!

I get really excited by decentralized systems and peer-to-peer networks because they have tremendous potential to empower individuals. I'm a lot less excited by traditional centralized systems and client/server networks, but that's because of how they've manifested in practice. Centralized, client/server systems defer power and authority to the server, and that's problematic when the server is controlled by a self-interested business with incentives that are misaligned with that of its service's users.

Despite the drawbacks, centralized systems have numerous technical advantages:

- Simplicity
- High performance
- High availability

Decentralized, peer-to-peer systems are great because they keep control and authority with the users. In a decentralized system, individual nodes (users) manage their own data and identity. However, these advantages come with tradeoffs:

- High complexity
- Unreliable availability
- Significant collective maintenance burden

These are fundamentally limiting issues. Enthusiasts will put up with the challenges of participating in a decentralized system, but typical users will not. If a product is going to achieve widespread adoption and enjoy the network effect benefits that brings, it needs to be approachable to the majority of people.

The ideal between these two extremes is a system that has the benefits of both without the drawbacks of either. Here's what I think that could look like:

- Dumb servers
- Smart clients
- Public key identity

Let's break down what each of these mean.

## Dumb servers

The fundamental problem with platforms like Google and Facebook is that the service knows _everything_ about its users. An alternative that actually keeps users safe is a service that knows _nothing_ substantial about them. This can be achieved through [end-to-end encryption](https://en.wikipedia.org/wiki/End-to-end_encryption). This is where alternatives such as Proton Drive shine: The service delivers significant value to its customers, but it doesn't monitor them because it's designed such that _it can't_.

A more user-centric model of cloud software is one where services do little more than store encrypted data that only clients can decrypt and utilize. For that to work well, we need smart clients.

## Smart clients

There has been a decades-long shift away from independently-functioning software that lives on user's machines and towards a model where clients are only focused on managing the user experience rather than business logic.

End user devices are quite powerful these days and there's no reason we can't have them execute substantial business logic. Given that, and the fact that we apparently can't trust cloud providers to access and work with our data, it's worth considering a shift back to a model where clients do the heavy lifting and treat the server as a functional enhancement (such as for data redundancy) rather than a requirement. This is a core tenet of [local-first software](https://www.inkandswitch.com/local-first/), and it fits elegantly with the concept dumb servers that only store end-to-end encrypted data.

## Public key identity

While Proton offers an excellent privacy-oriented cloud solution, it still requires a username and password to register. Like Google and Facebook, this relinquishes ownership of the user's identity to the service. We've normalized this model of software, but that doesn't mean it's a good one. People should be able to own their digital identity and not have to depend a on third-party to authenticate them.

Fortunately, there is an effective, established, battle-tested alternative: [Public key cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography)! It allows a user to create and provably attest their unique identity. When done correctly, it's effectively impossible for one person to impersonate another person's cryptographic key pair.

There are two significant drawbacks with public key cryptography:

- It's not intuitive to most people and never will be
- Effective key management is critical and challenging

These may be the major reasons that public key cryptography is not more widely used for identity. But in recent years, a solution to these problems has been developed: [Passkeys](https://www.passkeys.io/)! Passkeys completely encapsulate the complexities of public key identity and automate away the burden of key management. [WebAuthn](https://webauthn.io/) is the implementation of Passkeys for the web, and hopefully we will see increased adoption of it.

Rather than provide a username and password to web services when registering, users could instead provide public key credentials via WebAuthn and keep their real identity private. This is a better model, because it's safer and ultimately simpler for users. Passkeys can be backed up to a trusted cloud-based system of a user's choosing, and they don't need to worry about remembering usernames or passwords. All they have to do is present biometric identification (such as a fingerprint or facial scan) and they have access to their account.

---

## A future we can have if we choose it

We have normalized cloud services knowing everything about us and having total control over us online. This is a risky way to live, as our digital existence is based on little more than hope. Hope that Google and Facebook won't misuse our data (either intentionally or accidentally), and hope that we don't run afoul of capricious and byzantine service policies.

Many people are comfortable with the status quo, and they probably always will be because it's familiar and works well most of the time. But not everyone wants to settle for the status quo. There's always room for alternatives to exist and thrive, and there's always an audience for more sophisticated way of doing things. Along with the mainstream options like Google and Facebook, we can have more advanced cloud services that are designed around end-to-end encryption and public key identity. **We just have to choose to build something better.**

This is a future that I personally want to see, so I'm building my own expression of what that might look like. I'm developing [Passway](https://github.com/passway-project/passway/wiki/Passway-architecture), an API designed around end-to-end encrypted storage and public key identity. My long-term goal is to build a cloud that does everything for you, but knows nothing about you. It's very early days for the project, but I hope to see it or something like it become a common model for cloud computing. Wish me luck!
