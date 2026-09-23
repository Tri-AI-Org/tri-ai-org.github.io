---
title: "From Signal to Structure: TRI AI Cohort 10 Completes Course 3 of Google
  DeepMind AI Research Foundations"
date: 2026-09-23
division: teaching
excerpt: A progress diary from the TRI AI Saturdays organising team
draft: false
---
In our [previous post](https://tri-ai.org/blog/from-raw-text-to-meaning-cohort-10-completes-course-2/), we told you how Cohort 10 turned raw multilingual text into vectors a model could reason about, wrapping Course 2 with tokenizers built from scratch and words clustering by meaning in vector space. After a well-earned Week 7 break after an intensive six weeks of learning and going through courses 1 & 2, the cohort came back for a different kind of challenge: not how to represent language, but how a model actually learns.

That's the story of Course 3: Neural Networks & Training, covering Weeks 8 to 10. It's the course where the cohort moved from watching meaning emerge as geometry to watching models learn that geometry themselves, one gradient update at a time. It was also the course where Cohort 10 stopped being a screen-based community and started showing up for each other in person, in Lagos again and, for the first time, in Ibadan too.

**Week 8: When a Model Learns Too Much (or Not Enough)**

Lab - [Timi Owolabi](https://www.linkedin.com/in/timi-owolabi), ML Engineer, Quidax | Lecture - [Femi Azeez](https://www.linkedin.com/in/azeez-oluwafemi/), Co-founder, TRI AI

Course 3 opened on July 22 with a question every learner would spend the next three weeks wrestling with: how do you know when a model has actually learned something, versus when it's just memorized the answers?

Wednesday's lab, led by Timi, grounded the cohort in the bias-variance trade-off through a hands-on comparison: the same model trained for 10, 400, and 1,000 epochs. The 10-epoch version underfit, too simple to capture the patterns in the data; the 1,000-epoch version overfit, memorizing noise instead of signal; the 400-epoch version struck the balance. Participants worked through validation loss versus test loss, learned why the two serve different purposes in the training pipeline, and closed the day by rebuilding the fundamentals of neural networks from the ground up in NumPy. They tried their hands on perceptrons, activation functions, and the reasoning for why a network needs more than one layer to learn anything complex.

Saturday's lecture came with a twist: Due to the unavailability of Timi, TRI AI’s co-founder, Femi Azeez stepped in himself. If anything, it raised the stakes. Femi took the cohort through the deep learning revolution from AlexNet's 2012 breakthrough to the 2017 "Attention Is All You Need" paper that would, a few courses from now, become the cohort's own destination. Then he grounded it all in a simpler idea: the difference between signal and noise. A model that generalizes has learned the signal; a model that overfits has memorized the noise, and the gap between training and test accuracy is where that shows up. The lecture closed with something the room had been waiting for: the capstone project tracks. Nine projects went live, spanning legal advice, medical advice, African folktales, agriculture and climate, document retrieval, Toxicity detection, complaint classification, and finally,bridging the tokenization gap for African languages.

The Lecture this day also coincided with TRI AI Saturday Cohort 10’s first meetup outside Lagos. It was held at the Faculty of Computing, University of Ibadan, led by Ganiyat Oyeniyi with support from Mr. Ahmed, a Lecturer at the University of Ibadan and Founding Member of AI Saturdays Ibadan. Twenty-five participants showed up, a clear signal that this community's reach was outgrowing a single city.

**Week 9: The Shape of Learning**

Lab & Lecture - [Chimdi Walter](https://www.linkedin.com/in/chimdi-walter-ndubuisi-518607158/), PhD Researcher, University of Missouri Colombia

Week 9 belonged entirely to Chimdi, who took the cohort from "why do straight lines fail?" through to "here's the thing that doesn't fail", the multilayer perceptron.

Wednesday's lab pushed past linear models directly, showing participants how a straight decision boundary simply cannot separate non-linear data, and how stacking hidden layers with activation functions like ReLU and sigmoid lets a network carve out far more complex boundaries. Participants experimented hands-on: adjusting hidden layer sizes, learning rates, and epoch counts, watching how each choice reshaped the training and validation loss curves. Chimdi drew a clean line between parameters (what the model learns) and hyperparameters (what the practitioner sets), and introduced the toolkit for keeping a model honest: early stopping, dropout, regularization, and, when all else fails, more data. A memorable framing on data splitting was shared: train on the first 70% of a textbook, test on the rest, and you can trust the split because it still comes from the same distribution without being identical to what the model has seen.

Saturday's lecture, "Modeling Complex Data with Multilayer Perceptrons," made the case for why this moment mattered more than it might have seemed. Chimdi opened with real, local examples of non-linearity, okada fare surges that curve with distance and time of day, crop yields that rise then fall with rainfall, fraud that deliberately hides near normal behaviour, and language itself, where "I withdrew money from the \_\_\_" and "I fished by the \_\_\_" both end in "bank" but demand completely different predictions. He walked through AI history's first real scare: Minsky and Papert's 1969 proof that a single-layer perceptron can't even solve XOR, a result that nearly ended neural network research until backpropagation and hidden layers revived the field in 1986. The lesson, as Chimdi put it, wasn't that the field needed more data or faster hardware, rather, it needed depth and non-linearity.

From there, the session built out the anatomy of an MLP layer by layer, live in TensorFlow Playground, watching a decision boundary bend the moment a hidden layer was added. It circled back to overfitting, and this time through the lens of a chatbot that aced its training examples but failed real customers. The failure was because it had learned a coincidental, meaningless pattern instead of the actual signal. The validation set's role is explicit: train to learn, validate to choose, test only once, because tuning against the test set is just "slowly lying to yourself." Chimdi closed with a section that felt new for the cohort: alignment and safety. A model optimizes exactly the loss it's given, nothing more. This  means a loan-approval model trained on biased historical decisions will learn that bias faithfully and confidently. The session's homework asked each participant to write their own short safety test for a model built for their own community: what examples would you check, who's involved, and what would success actually look like? It was also a quiet signal of where the course was heading, and Chimdi noted that the MLP the cohort had just learned is, almost unchanged, the feed-forward block sitting inside every transformer layer, the same architecture Femi had name-dropped back in Week 8.

**Week 10: Gradients, Ibadan, and a Room Full of Mentor**

Lab & Lecture - [Fortune Adekogbe](https://www.linkedin.com/in/fortune-adekogbe/), PhD researcher, University of Michigan 

Week 10 was where the calculus finally showed its face. The facilitator for the week, Fortune, took the cohort from "how do models learn?" to "here is the actual mechanism" in Wednesday's lab (Aug 5). He spoke on derivatives, partial derivatives, and gradients as the compass pointing the model toward lower loss. Working through JAX-based exercises, participants watched adjusting a single weight or bias visibly reshape a decision boundary, then built a small classifier from scratch, tracking its loss drop from 0.75 to 0.67 after a single gradient update. The Adam optimizer got its first introduction here too, showing a taste of why "remembering" past gradients helps a model converge faster than plain gradient descent.

Saturday's lecture (Aug 8) continued into loss landscapes, convex versus non-convex optimization, and a clear-eyed tour of activation functions like ReLU for hidden layers, sigmoid and softmax for output layers, and why stacking linear layers without activation functions in between gets you nothing but a more expensive linear model. But the day ran out before reaching one of its planned centerpieces, backpropagation, so a follow-up session was scheduled for Monday, August 10 at 7pm to finish the job. 

During Monday’s session, Fortune walked the cohort through the forward and backward pass in full: how the chain rule assigns "blame" to every weight in the network, and how that gradient is then used to actually update the model. He laid out the spectrum of ways to do that update, which includes full-batch, stochastic, and mini-batch gradient descent. He also explained the optimizers built on top of it: momentum for smoothing noisy gradient steps, RMSprop, and Adam, which combines both direction and scale memory and remains the sensible default. The session closed on a note that echoed Chimdi's Week 9 lecture almost exactly: loss alone doesn't tell you if a model generalizes, and building responsibly means staying alert to a model's social impact and the biases it might carry, particularly in language and facial recognition systems.

Saturday itself, though, was memorable for more than the material. It landed the day after Deep Learning Indaba wrapped, and a good number of community members who'd been at DLI carried that energy straight into the Second Lagos meetup held at NitHub, University of Lagos, with 44 people in the room, including a strong TRI AI team presence: co-founders Tejumade Afonja and Oluwafemi Azeez among them, alongside other team members. It also included Mentors like Kosi and Moses on the call where they were answering questions participants have regarding the projects.

**Where We Stand After Three More Weeks**

Ten weeks in, and the cohort has gone from cleaning multilingual text to building tokenizers to now understanding, from first principles, how a neural network actually learns, which involves bias, variance, gradients, activation functions, and the judgment calls that separate a model that generalizes from one that merely memorizes. And for the first time, that learning spilled fully offline: two in-person meetups in two cities, mentors in the room answering questions in real time, and co-founders showing up alongside the community they built.

With projects now underway across all nine tracks, the road ahead turns toward the architecture that makes today's large language models possible. Course 4: Transformer Architecture will take the cohort into attention mechanisms and positional encoding. The same MLP block the cohort just learned to build is now wrapped in attention, and the ideas the whole cohort has, in a sense, been building toward since Week 1.

We'll be back for the Course 4 wrap where we’ll be exploring the transformer architecture. Until then, to every learner who debugged a gradient at midnight, showed up to defend a decision boundary, or traveled to a room in Ibadan or Lagos to meet the community behind the screen: thank you for building this with us.

*\- The TRI AI Saturdays Cohort 10 Organising Team*

 Jesuyanmife Egbewale, Programmes Volunteer
