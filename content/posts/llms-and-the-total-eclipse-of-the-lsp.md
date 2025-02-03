+++
title = 'LLMs and the Total Eclipse of the LSP'
date = 2025-02-03T01:59:41Z
draft = false
+++

_Or, why I'm a grumpy old man who thinks they don't make them like they used to_

Welcome to 2025. LLMs have captured the hearts and minds (AKA VC dollars) of everyone and they are literally the only thing happening at all in the entire tech industry. They are the cause of and solution to every problem and will both save and destroy the world.

LLMs are at least a potential solution for a very wide range of problems, but they're often not the best and very rarely the simplest. The one thing you can say for sure with LLMs is that you can put stuff into them, and _something_ will definitely come out. Will it be the right thing? Who knows, hit the button and see what happens!

Hitting the button and seeing what happens is a fine workflow for a lot of situations. It's great for creative writing, drafting Jira tickets, cheating on homework, and writing emails to people you don't care about. But some work requires a bit more determinism. Programming is an example of such work; either software works correctly or it does not. Because we live in the future, LLMs are quite good and will often provide you with code that at least _mostly_ works. And if you already know how to write the code you're asking the LLM to write, then you'll be able to verify the output and grin smugly about all the time you just saved yourself (or regenerate the response five times and then give up and just write it yourself in frustration). If you don't already know how to write it yourself... well, hopefully somebody catches the bugs in code review.

What makes LLMs both great and terrible is that they hallucinate. It's not a bug, it's the very essence of what they exist to do. LLMs don't actually know anything and mostly don't have access to any kind of database of verifiable information. They are machines that were shown a lot of information in training and learned to infer new conclusions based on the patterns they picked up in that training. But they don't _know_ anything. They have no truly concrete way to validate nontrivial assumptions or conclusions. They're just making extremely educated guesses. And they're doing it in an extraordinarily resource-intensive way.

I like LLMs ([at least ones that I can run on my own personal hardware](/posts/local-ai-is-the-only-ai/)), but I'm also a simple man who enjoys simple things. A resource-intensive guessing machine is not the simplest solution for a majority of programming-related tasks. Such tasks include writing, refactoring, finding and moving code. Ironically, this problem has been well-solved by long-established, proven static analysis tools that predate LLMs by decades. Linters, for example, are static code analysis tools that deterministically evaluate code and identify a wide range of problems. They're not as versatile as LLMs, but they are completely consistent and reliable and very often versatile enough.

In the mid-2010's, Microsoft gave the world a wonderful gift: The Language Server Protocol, or LSP for short. At a high level, LSPs are a unified way for code editors such as Neovim to communicate with a wide range of development tools. That doesn't sound particularly exciting, but it's the technology that tells you what properties or methods the object you just typed has available to it. This is _a little_ more exciting, but still not exactly compelling. More advanced LSPs (such as the ones available for TypeScript) offer advanced refactoring capabilities such as extracting functions, moving code to different files, renaming variables (across files!), finding code references and definitions, and more.

There's a good chance you're sitting there rolling your eyes because you know that LLMs can do this too. But hold on there, buddy. Your LLM takes _an extraordinary_ amount of compute to do this work. And if you're not running it on a $20k custom-built NVIDIA rig that heats up your whole house, then you're paying someone like Anthropic to do it in a data center. LSPs, on the other hand, can do this work on any random laptop purchased from Walmart. And the best part? LSPs don't hallucinate! They literally can't! They will always provide you with a valid response, unlike LLMs which may or may not.

LLMs definitely have their place. But they aren't the only solution to most problems, and are very rarely the best. For many programming tasks, LSPs are just as good of a solution and much more efficient. New tools don't have to replace old ones, they can supplement them too! I have no problem using LLMs in my workflow, but I use LSPs far more frequently because they're faster and better for real-world scenarios. And the best part? I don't have to provision a server rack or fund a new yacht for Sam Altman to use them.

Long live LSPs!
