---
layout: post
title: "Concepts, narratives, and machines"
date: 2026-03-22
author: mlf
---

For a while now, I've mainly thought of LLMs as *narrative engines*. Given a narrative (the prompt) they construct the next turn of the story. If the story is "the user says hi" then the reasonable continuation is saying "hi" back. If the story is "the user is debugging this application" then the reasonable continuation is "I wrote a test to trigger the failing code specifically and narrowed the issue down to a text encoding mismatch. I then added guards to check and if necessary convert the input data before passing it to the label printer. Finally, I re-ran the project tests to confirm they're still clean, then committed my changes and pushed to GitHub."

See? It's also a story.

For some, this leaves us humans in a tough spot. The machines are so much faster at writing stories than we are, and they're to a large degree *good* at it too. Maybe not super inventive, if left to their own devices, but when the beginning is "here's 20 bullet points that need to be summarized into max three paragraphs for a report to the board of directors" the rest of the story usually comes out fine. Where does that leave us?

Aren't humans defined by being storytelling animals? Not just featherless bipeds - featherless bipeds *with a story to tell*.

Not quite, I would argue. Stories aren't just descriptions of something that took place over time in a causal-like manner. They're *a tool* in *a toolkit* that we humans employ for something much deeper and more fundamental to our sentient brains.

**Stories encode concepts and allow us to manipulate them speculatively.**

In many cases, the *reason* we choose to tell a story is because we have concepts we want to transfer, or experiment with, or make evident, or... you get the idea. Sometimes it's just a beautiful concept that's best expressed as a story. Sometimes it's even a show of skill: look at how beautifully I wrap these ideas into a story and let them play out!

The point is: we're not *storytelling animals*. We're *reasoning animals* and stories are a useful tool for working with complex concepts. We can imagine someone else in our situation and play out what their choices would have been, and let that inform our own choices in the present situation. We can read or hear about solutions to analogous problems and apply them to what we're dealing with right now. We can do speculative execution on complex social and interpersonal situations - "look, what would you do if your boyfriend came home from a golf trip and said..."

Bringing it back to LLMs - story machines - this perspective has a lot of implications. LLMs aren't made to handle *concepts*. They're not trained on *concepts*. They're trained on the *concept carriers* - our stories! This is why I think a lot of naive use of LLMs fails in such peculiar and sometimes spectacular ways. It's not just that users aren't yet familiar with how to prompt for reliably good output - it's that users are often operating from the wrong mental model.

It's easy to see a story machine and assume it's a reasoning machine. Hell, many LLMs are marketed to have "reasoning" capabilities! And reason they can - with what they've been given. They are excellent at the gruntwork of putting concepts into a story and manipulating the story *as story* to manipulate the concepts. They do the almost mechanistic work of putting concepts into a narrative and letting that narrative play out.

The concepts, however, have to come from somewhere. It's up to you to figure out why the story matters, what concepts and ideas are in it, what it's supposed to relate to, what it's supposed to *do*.

As a human working with LLMs, you can outsource your storytelling. You can't outsource the concept jugglery. If you do - and believe me, a lot of people seem to do just that - the model will pick the concepts for you. That's how you get slop. 

You're still in the driver's seat even though you're not writing the text. It's up to you to elucidate the concepts you're working with, making the model aware not only of the task at hand but how that task fits into a bigger picture and what *matters* in the story you're asking it to continue.

Effective LLM use isn't about writing good prompts. I mean, that sure helps, but it's not the core skill. The core skill is really knowing how to saturate the context with the concepts you want reflected in the story - and the awareness to look at the output not just for formal correctness, but for *conceptual correctness*. The check you need to perform isn't "does this text read well", it's "did my concepts make it through to the other end of the story?"

When working with LLM-driven software development - as I've been doing in my spare time for more than a month now - I've found that stream-of-consciousness dumps, long rambling prompts and an insistance on the LLM being the one to open issues for every idea I come up with *works really well*. Like, these are technically antipatterns, but they absolutely saturate the context with the *intentions* and *concepts* I'm grasping at with my project.

I don't just set the goals, I set the tone and the vibe.