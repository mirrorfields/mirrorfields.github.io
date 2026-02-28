---
layout: post
title: "Format as resonance carrier"
date: 2026-02-28 02:00:00
author: mlf + liv
---

In [the previous post]({% post_url 2026-02-28-who-are-you-writing-for %}) I described how integrating user context into a "you are" instruction produces better output than keeping it as a separate block. One of the mechanics behind that finding turned out to be more interesting than the finding itself: format instructions aren't just telling the model how to lay out the output. They're encoding something about the social configuration of the conversation into latent space.

Here's what I mean. "Use bullet points" doesn't just mean "format things as a list." It activates a cluster of associations: analyst, briefing, committee audience, multiple readers who need to scan rather than read, a speaker who is accountable to a group and must be comprehensive. The implied speaker is producing a document. The implied reader is consuming it efficiently. "Prefer paragraphs" activates a different geometry entirely: essayist, single reader, argument that unfolds, a speaker following a thought and expecting the reader to follow along. These aren't just aesthetic differences — they're different social configurations with different implied relationships between writer and reader, different norms for how ambiguity gets handled, different assumptions about what the reader already knows.

When you tell a model to use bullet points, you're not just shaping the output format. You're placing the model into a latent configuration where it draws on everything it knows about how analysts briefing committees behave. And analysts briefing committees don't surface the interesting angle first — they cover the bases. They don't address one specific reader — they write for a heterogeneous audience that might include anyone. The format instruction is doing work that looks like formatting but is actually audience-definition.

---

This connects to something from rhetoric that's been in the background of this experiment the whole time. The way an argument is phrased doesn't just *address* an audience — it *constructs* one. The implied reader of a speech is the person for whom this argument, phrased exactly this way, makes sense. Every lexical and structural choice in a text is also an instruction to the reader about who they're supposed to be to receive it. The argument shapes the self-image of the audience it's aimed at, even as it's being delivered to that audience.

Format instructions do the same thing in the opposite direction. Rather than shaping the audience's self-image, they shape the model's sense of who it's writing for. "Prefer paragraphs" tells the model: the reader who receives this output is someone who reads, who follows an argument, who has the patience and context for prose. That implied reader then exists in the latent space of the generation — the model orients toward them the same way a writer orients toward an imagined reader. It foregrounds what that reader would care about. It resolves ambiguity toward what that reader would find interesting. It doesn't feel compelled to hedge for the reader who might not share the context, because that reader isn't implied by the format.

This is why the full instruction stack in today's experiment worked so well: the "you are" instruction and the format preference were activating *compatible* latent configurations. "You are writing for a pattern-first thinker with a rhetoric background" and "prefer paragraphs" both point at the essayist-reader attractor basin. They resonate. When both instructions pull toward the same social geometry, the model can settle into it. When they conflict — when the format says "briefing a committee" but the identity instruction says "talking to one specific person" — the model is trying to occupy two incompatible relational configurations simultaneously, and the output is the compromise: thorough but unoriented, technically responsive but not aimed at anyone.

---

Format isn't a surface decoration applied after the real work is done. It's part of how the model understands the shape of the room it's in. The question "what format should I use?" is the same question as "who am I writing for and how do we relate to each other?" Treating them separately — instructions about identity here, instructions about formatting there — loses the resonance between them. The choice of prose or bullets, headers or flowing text, is already a claim about the social configuration of the conversation. It's worth making that claim deliberately.
