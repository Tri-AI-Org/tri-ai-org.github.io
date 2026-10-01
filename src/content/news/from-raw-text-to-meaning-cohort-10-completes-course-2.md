---
title: "From Raw Text to Meaning: Cohort 10 Completes Course 2"
date: 2026-08-19
division: teaching
excerpt: |
  A progress diary from the TRI AI Saturdays organising team
draft: false
---
Last time, we told you how [Cohort 10 wrapped Course 1](https://tri-ai.org/blog/three-weeks-in-how-cohort-10-learned-to-think-like-a-language-model/); Participants trained their first small language model and learned to think in n-grams and probabilities. Since then, the cohort has moved from *"how do language models predict the next word?"* to a much more hands-on question: **how do you turn raw, messy, human text — in dozens of languages — into something a model can actually learn from?**

That's the story of **Course 2: Text Data - Tokenization & Embeddings**, covering Weeks 4 to 6. It's the course where the cohort got its hands properly dirty with data, wrestled with what "fair" AI means for African languages, and by the end, watched words turn into vectors that a computer could reason about. Here's how it went.

## **Week 4: The Soul of a Language, One Preprocessing Decision at a Time**

**Lab & Lecture — [Foutse Yuehgoh](https://www.linkedin.com/in/foutse-yuehgoh-phd-9105b184), AI Researcher**

Course 2 opened on June 24 with a guest instructor, Foutse Yuehgoh, leading a live coding session that immediately set the tone for the weeks ahead: **preprocessing text is never one-size-fits-all.**

In the Wednesday lab, Foutse walked participants through cleaning multilingual text data, and almost immediately, the "obvious" cleaning steps stopped being obvious. Should you strip accents? Not if you're working in Yoruba, where an accent changes the meaning of a word entirely. Should you remove "duplicate" lines? Not so fast, in Persian, what looks like a repeated word can actually be a completely different one because of subtle letter variations invisible to an untrained eye. Working through examples in Swahili, Amharic, Yoruba, Arabic, Igbo, and Persian, the cohort learned a lesson that would echo through the rest of Course 2: **you cannot clean a language you don't understand.** Every preprocessing choice; what to trim, what to normalize, what to preserve, has to be made with the language and its context in mind, ideally in conversation with the people who speak it.

Saturday's lecture pushed this further into territory that felt less like a coding class and more like a conversation about justice. Foutse explained why low-resource languages end up "costing more" computationally; their unfamiliar character sets and patterns mean tokenizers need more tokens just to represent the same sentence a European language would express more cheaply. The class then turned to a harder question: **who owns the data that trains these models?** Foutse walked through the murky reality of web-scraped datasets, how it's often nearly impossible to trace consent after the fact, while making the case that going forward, responsible data collection means documenting sources, respecting licensing, and investigating local laws rather than treating scraping as a free-for-all. A live poll asked the cohort whether undocumented datasets could be trusted; the room overwhelmingly said no, and a good discussion followed about why documentation, not just existence of data, is what builds accountability.

The session closed with a first look at project life ahead: Capstone Lead Joscha Cüppers introduced the six project tracks teams would eventually choose from — spanning legal advice, medical advice, African folktales, agriculture and climate, and document retrieval — while our organising team worked behind the scenes to reshuffle teams based on real activity levels, so that engaged learners would be grouped with equally engaged teammates ahead of project work. It was also the week we announced our first in-person meetup plans for Lagos — the first sign that this cohort wouldn't stay confined to a screen.

## **Week 5: Teaching a Computer to Read, One Byte Pair at a Time**

**Lab & Lecture — [Abdulsamad Baruwa](https://www.linkedin.com/in/steloy/), AI Engineer, Steloy AI**

If Week 4 was about *cleaning* text, Week 5 was about *breaking it into pieces a model can actually use* — tokenization.

Wednesday's lab, moderated by our own Israel Ekundayo, opened with participants sharing one-word check-ins — "fantastic," "inspired," "ready" — before Abdulsamad took the room through the building blocks of tokenization: character-level splitting, word-level splitting, and then the technique that Course 2 had really been building toward, **Byte Pair Encoding (BPE)**. Despite some audio and connectivity hiccups along the way (a familiar hazard of running live sessions for hundreds of people across the continent), Abdulsamad broke BPE down into a clear four-step process: add end-of-word markers, find the most frequent adjacent pairs in the text, merge those pairs into new tokens, and repeat. Participants like Olugbenga and Oscar worked through the logic live, discovering firsthand why words like "desert," "deserted," and "desertion" share common sub-word building blocks — and why that matters for how efficiently a model can represent language it has never seen before.

Saturday's lecture took the theory further and, honestly, delivered one of the most important sessions of the cohort so far. Abdulsamad explained why BPE became the standard for models like GPT and BERT — it strikes a balance between vocabulary size and sequence length that pure character or word tokenization can't. He introduced how tokenizers are actually evaluated: **intrinsic metrics** like fertility (how many tokens does it take to represent a word?) and parity (is that cost fair across languages?), versus **extrinsic metrics** that only show up once a full model is trained. Then came the number that stopped a lot of people in their tracks: of Africa's roughly 517 languages, only **45 are represented in existing NLP benchmarks** — fewer than 10%. Abdulsamad was clear that this isn't a complexity problem, it's a *data and investment* problem, and closing that gap will take more than clever algorithms — it needs engineers, policymakers, and domain experts working together. It was a fitting continuation of Week 4's "who owns the data" conversation, now backed by hard numbers.

On the logistics side, this was also the week we opened up team representative selection to keep communication flowing smoothly across hundreds of teams, and announced our first Lagos meetup for the following Saturday — a watch party of the online class with real-world networking and refreshments.

## **Week 6: Where Words Become Numbers**

**Lab & Lecture — [Kaletsidik Ayalew](https://www.linkedin.com/in/kaletsidik-ayalew/), AI Engineer**

Week 6 was the finale of Course 2, and it delivered on the promise the whole course had been building toward: **embeddings** — the step where tokens stop being arbitrary IDs and start carrying meaning a model can reason about.

Wednesday's lab, once again anchored by Israel Ekundayo before handing over to Kaletsidik, tied together everything the cohort had learned since Week 2. Kaletsidik walked through the full pipeline in one sitting — n-grams, text processing, tokenization, and the specific tokenizers (BPE and TikToken) the cohort had already built by hand — and framed the big picture clearly: a language model is fundamentally a *next-token prediction system* that learns useful embeddings and relationships between tokens so it can get better at guessing what comes next. The session's own recap put it best: raw text goes through tokenization, becomes token IDs, gains embeddings and position information, makes a prediction, calculates its error, and updates itself — over and over — until it generates coherent text. It was the moment several strands from the last three weeks visibly clicked into place for a lot of learners.

Saturday's lecture was, in every sense, a milestone — our **first in-person TRI AI Saturdays meetup**, hosted in Lagos, with more than 30 people showing up in person alongside the usual online crowd. Adetola opened with something the whole team was proud to share: TRI AI's story, from its founding as AI Saturdays Lagos in 2018 by Teju and Femi, to today's community of over **10,000 members** and **10 completed cohorts** — with Cohort 10 alone bringing in 3,000+ registered participants. Students introduced themselves from backgrounds as varied as agricultural extension, law, and engineering, a reminder of just how wide the appetite for AI skills has grown across the continent.

Then Kaletsidik took the technical wheel, teaching embeddings from first principles: how words become vectors, how **cosine similarity** measures the "angle" between two ideas, and how techniques like **t-SNE** and **PCA** can flatten those high-dimensional vectors down to a 2D map you can actually look at — where words like "dog" and "puppy" cluster close together, while unrelated words drift apart. The room worked through live vector calculations by hand — dog and tree, dog and man, man and woman — cementing something that can otherwise feel completely abstract: *meaning*, in a language model, is really just geometry.

With that, Course 2 was officially complete — and so was the cohort's introduction to how text becomes something a machine can learn from.

## **Where We Stand After Six Weeks**

Six weeks in, and the cohort has gone from predicting single words with n-grams to preprocessing real multilingual datasets, building a tokenizer from scratch, and mapping meaning as vectors in space; all while wrestling with genuinely hard questions about representation, consent, and fairness for the languages of this continent that global AI too often leaves behind.

Behind the scenes, our organising team spent these three weeks doing the unglamorous work that keeps a cohort of this size moving: fixing a broken mailing list mid-course, processing over 900 team-reassignment responses to keep teams active and balanced, chasing down Discord access issues, and pulling off our first-ever in-person meetup in Lagos.

Week 7 comes next: a well-earned mid-cohort breakfor teams to catch their breath, finalize project selections, and connect with mentors, before **Course 3: Neural Networks & Training** kicks off in Week 8, taking the cohort into MLPs, backpropagation, and gradient descent.

We'll be back for Course 3 wrap. Until then, to every learner who debugged a tokenizer at midnight, sat through a hard conversation about data ethics, or showed up in person in Lagos to meet the community behind the screen: thank you for building this with us.

*— The TRI AI Saturdays Cohort 10 Organising Team*

**Israel Ekundayo, Programme Volunteer**
