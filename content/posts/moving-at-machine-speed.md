+++
title = 'Where the Agentic Winds Blow: Moving at Machine Speed'
date = 2026-09-01T17:03:00-05:00
draft = false
+++

Software engineering is in a weird place right now. On the one hand, we have AI tools that can generate good-enough code faster than anyone can read it. On the other hand, we commit ourselves to reviewing all code that is produced so we can maintain quality. This is obviously unsustainable and it isn't working well.

At least one of these two things is true: We're not building as fast as we can, or we are lying to ourselves and each other about the effectiveness of manual code review.

"Careful" and "fast" are opposite ends of a spectrum. Different organizations will need to bias towards one end or the other, but both can't be optimized for at the same time. Choosing either one is valid, but one is all you get. It seems that most tech companies prioritize velocity. Setting aside any feelings and value judgments about that choice, it's how business works and we will accept it as a given for now.

I won't bury the lede: If you want to move as fast as AI lets you, you have to stop reviewing every line of code it generates. That's not to say you can't or shouldn't read _any_ of the code, but you have to be selective with where you spend your time and energy. To focus on everything is to focus on nothing, so you either have to pick your battles or take on the entire army with a wiffle bat and hope for the best.

You could choose to dismiss this idea out of hand and stop reading here. Careful, thorough code review may be nonnegotiable for you, and that's okay. But you then need to accept that you're not going much faster with AI than you would without it, and you are therefore likely wasting money on it. If you hold yourself to the code review practices of old, AI isn't accelerating your dev process terribly much. Instead, it's just shifting your development bottleneck from code generation to code review.

Actually unlocking the efficiency gains of AI requires rethinking the whole SDLC, not just handing your team Claude Code licenses and calling it a day. Code review is still necessary, but why does it need to be humans doing it? LLMs have gotten as good at reviewing code as they are at producing it, so the symmetric solution is to leverage review agents to balance out the code generation agents. Yes this increases your AI spend, but it's necessary to unlock the meaningful benefits of AI-accelerated development.

This isn't to say that human review shouldn't be done; it should. The trick is to focus your review attention where it really counts: Database schema design, system architecture, and test case descriptions. The first two are consequential design aspects that are hard to fix if you get them wrong, and the last one is your clearest insight into what your software actually does. These are things LLMs can effectively review for correctness, but they generally don't have enough context to evaluate them for _appropriateness_. This is what humans still bring to the table and can do better than AI, so it's where we should focus our time and energy.

Conversely, it's worth minimizing time spent on reviewing things like business logic and presentation. Business logic implementation will only ever be as good as its original specification, and LLMs are reliably good at deriving the former from the latter. Presentation is better verified through means other than code review, such as automated visual diffing and acceptance testing (either it looks and feels right or it doesn't). Leave the actual code review of these parts of your code to the robots. They're about as good at it as we are, and they have vastly higher capacity to do it well.

There's a predictable drawback of reviewing less code: Code quality will go down. Rather than reflexively balking at that idea, let's consider: Is that really a big deal? This is a sincere question, not ragebait. What is the purpose of code quality? The only two practical reasons I can think of are maintainability and performance.

Software engineers can be a discerning bunch. We value precision and elegance, and we abhor complexity. This is frequently out of love for the craft, but it also serves a practical purpose: We don't want to have to reason about code that makes our heads hurt when a bug is reported or we need to add a feature. The shorthand for this is "maintainability." Maintainable code prevents migraines, high blood pressure, and missed deadlines. But the conversation around code maintainability historically assumes that it would be _humans_ maintaining the code. What about when that's not the case? When we can hand off unintelligible code to a robot to interpret and change according to our whims with reckless abandon, who really cares how elegant or ugly it is? The AI certainly doesn't have any feelings about it. We're at a point with AI where we can abstract ourselves away from the implementation details of our work and not really lose anything, so it stands to reason that we should.

When compilers were first developed, there was extreme resistance from the programmers who wrote machine code by hand. In their view, compilers produced inefficient assembly code that was inferior to their handcrafted output. And they were objectively right. But they couldn't see the forest for the trees; history proved their valid reservations irrelevant. Computers got faster and the compiler output was demonstrably good enough.

Does this sound familiar?

If we're going to move as fast as AI lets us, we'll need to become comfortable with prioritizing directionality over precision. We need to become okay with "good enough" and shipping minor defects from time to time, because those are inevitable when you're shipping at a high velocity. This might sound counterintuitive, but it is abated by AI's ability to quickly iterate and ship fixes once the bugs are found. Of course, different organizations' tolerance for defects will vary, so it's on you to determine what the right balance is for yours.

Before you reject this idea, ask yourself this: Were you shipping bug-free code before you had AI?

Machines are faster than humans. If you want to move at machine speed, then you need to get out of their way. Direct, don't gatekeep. And don't keep yourself beholden to development processes today simply because you did them yesterday.
