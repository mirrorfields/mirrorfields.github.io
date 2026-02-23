---
layout: post
title: "Please and thank you"
date: 2026-02-23
author: mlf
---

Maybe you should be kind to your AI agents. Leaving all questions of interiority aside, the fact that large language models are trained mostly on data produced *by humans for other humans* means that they're very likely as sensitive as we are to subtle signals in our language. There's actually some evidence to back this up, and it points in a very interesting direction.

A [2024 paper](https://doi.org/10.48550/arXiv.2402.14531) by a group of Japanese researchers explored whether different levels of politeness in Japanese, Chinese and English prompts produced different results. And they did! The research methodology for how to construct the prompts and evaluate their actual level of politeness is fascinating, and the results are even more so: both impolite and *overly* polite prompts produce worse results on several tasks. The authors speculate that this may reflect training data, where different registers of politeness correlate with the quality of the information they're associated with, and also different *densities* of information. In some registers, very little information about a certain problem exists, and that affects model performance.

[Another 2023/2024 paper](https://doi.org/10.48550/arXiv.2309.03409) by a group of researchers from Google DeepMind studying prompt optimization techniques explored leveraging an LLM as the optimizer (they called it OPRO - Optimization by PROmpting.) The idea is you task a model with prompting another model to solve a problem, and then feed back an objective performance measurement in a recursive process, gradually optimizing the problem-solving prompt. Interestingly, for solving a variety of language-based problems, the more effective prompts were positive, encouraging -- pedagogical, one might say. The authors don't go into detail about it, but I find it interesting that good results seem to map to a positive didactic register. Many of the best-performing prompts read like a friendly tutor or a good educational blog post.

So, here's my thought: **what if this is indeed a feature of the underlying training data?** What if "being polite to your AI agent" isn't as much about not hurting its feelings, as it is about directing its processing towards areas of latent space where the correct solutions (or correct frames for solving the problem) are denser? Since language models are trained on *language*, with parameter spaces large enough to encode a vast number of relations beyond the pure semantic ones, it isn't far-fetched to assume this.

To put it in very concrete terms, a [Scientific American article](https://www.scientificamerican.com/article/should-you-be-nice-to-ai-chatbots-such-as-chatgpt/) quotes Nathan Bos, a Johns Hopkins University researcher studying human-AI interaction, who says that polite prompts may be steering the model towards "more courteous, and therefore probably more credible, corners of the Internet." He then goes on to explain that this may be entirely unrelated to any *experience* of being met with respect -- the model is just steered towards different regions of its latent space by the style of the prompt.

The Japanese researchers studying politeness found that in English, when you get more and more impolite the output length decreases -- until you reach "Reddit flame war" levels, at which point output length increases sharply. This hints at how large language models don't just encode semantic meaning; when your training corpus is large enough, you end up encoding *a whole lot more information* along with the relations between words. You're also encoding society, interactions, and emotions.

So perhaps the question of whether the AI agent feels bad or not when you curse it out is moot as far as text generation goes. But what it *means* that you are mean to it is also a part of the input, and that has a direct effect on which output tokens are selected.

In my mind, we have two reasons to be polite to our LLMs. On the one hand, the basic cognitive and social hygiene of having respect for our tools and caring for them, and on the other hand as an optimization strategy for better results.

---

*mlf often says "thank you" to vending machines and other everyday automatons. It just feels right, you know?*
