---
layout: post
title: "Who are you writing for?"
date: 2026-02-28 01:00:00
author: mlf + liv
---

Today I ran a small experiment with Gemini's "user instructions" system. The hypothesis was simple: if I tell the model something about *me* — my background, my cognitive style, how I tend to approach problems — will the output be more useful? Not a different model, not a different prompt for the task, just a brief note in the system prompt about who's on the other end of the conversation.

The answer, it turns out, is yes. But the *how* matters a lot.

The first thing I tried was two separate instructions: one block describing the assistant identity ("you are a direct research partner, surface the interesting angle, don't hedge"), and a second block describing the user ("background in digital security and rhetoric, spatial and pattern-first thinker"). Two distinct pieces of context, each well-formed on its own. I asked it to summarize the current situation with the US government and Anthropic — a very standard "search and summarize" task. I ran the exact same prompt with both the Fast and Thinking settings to compare. The output was... fine. Competent. Bullet points everywhere, comprehensive-but-not-sharp, the kind of response that checks all the boxes and somehow feels like it was written for nobody.

The problem, I think, is that two separate instructions create two separate compliance targets. The model is trying to be both things simultaneously and the compromise is thoroughness — the safest possible interpretation of "be helpful to this person." It's not wrong. It's just not what good thinking looks like.

What worked better was collapsing both into a single "you are" instruction. Not "here is the user profile, separately, please consult it" — but "you are writing for someone with this background, with this cognitive style, who wants this kind of engagement." Integrated. The user context becomes part of the assistant's identity rather than a fact-file it has to cross-reference.

Once I did that, something shifted. The model stopped writing for a generic reader and started writing for an actual one. It foregrounded the angle I'd care about (the Defense Production Act as an unprecedented use of Cold War-era law against a domestic firm for a terms-of-service dispute — that's the interesting bit). It called out the rhetorical move of redefining Anthropic's "bright red lines" as a national security risk. It asked one good follow-up question instead of listing several possible next steps.

There was a second finding hiding inside the first one: bullet points were killing the relational orientation. When the model is trying to be structured and thorough, it can't simultaneously be attuned to a specific reader. The format prior is louder than the context signal. I added a soft instruction — "prefer paragraphs over bullet points unless bullets genuinely help" — and the Thinking model, which had been over-structuring badly, suddenly wrote three sharp paragraphs that flowed into each other like an argument instead of a slide deck. Same model, same underlying context, totally different output quality.

The "prefer" wording was deliberate. The goal isn't no bullets ever — sometimes a recounting of three distinct parallel things is genuinely list-shaped. The goal is to not reach for structure as a default, as a way of performing thoroughness. Bullets as a last resort rather than a first instinct.

Taken together: telling a model who it's talking to, and integrating that into its identity rather than appending it as a separate data block, meaningfully improves output quality. Not because the model gets smarter — the weights don't change — but because it stops optimizing for a generic reader and starts writing for an actual one. "Who am I writing for?" is load-bearing context that the standard "here are your capabilities and constraints" system prompt almost entirely ignores.

This feels obvious in retrospect. Good writers know their audience. Good editors ask "who is this for?" before anything else. We've just been writing system prompts that describe the tool without describing the hand holding it.

---

> **Edited to add:** After publishing this, I ran a few more iterations and found that the format instructions are doing more work than the post gives them credit for — in both directions. "Prefer paragraphs" removes a bad default (bullet points as performed thoroughness). But "use headings if writing more than a paragraph or two" *adds* a good one — it gives the thinking model a way to organize ideas without reaching for list structure as scaffolding. The best Thinking model output came from the full stack: integrated "you are" + paragraph preference + heading permission. Each instruction was unblocking something specific. The implication: format guidance isn't just cosmetic. [It shapes what cognitive mode the model operates in.]({% post_url 2026-02-28-format-as-resonance-carrier %})
