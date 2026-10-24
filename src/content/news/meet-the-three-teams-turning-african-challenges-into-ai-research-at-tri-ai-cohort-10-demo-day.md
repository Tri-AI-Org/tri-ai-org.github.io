---
title: Meet the Three Teams Turning African Challenges into AI Research at TRI
  AI Cohort 10 Demo Day
date: 2026-10-24
division: innovation
excerpt: Meet the Three Teams Turning African Challenges into AI Research at TRI
  AI Cohort 10 Demo Day
cover: /uploads/1001242918.jpg
draft: true
---
*From African language tokenisation to financial complaint analysis and mental health support, the three winning teams of TRI AI’s Cohort 10 Demo Day are exploring how AI research can address problems that matter to African communities.*

On Saturday, 3 October 2026, TRI AI hosted a live session for its AI Research Foundation Course 1-4 Cohort 10 Demo Day, where nine finalists presented projects they had developed during the programme. 

Three teams emerged as winners: Team Bangweulu in first place, Team Atbara in second place, and Team Chamo in third.

We spoke with the team leads about their projects, the challenges they encountered, what they learned during the course and what they hope to do next.

## Team Bangweulu: Rethinking How AI Processes African Languages

![Team Bangweulu](/uploads/1001242915.jpg "Team Bangweulu")

**Team lead:** Wiam Atfi

**Core development team:** Wiam Atfi and George Aladejana

**Early contributors:** Adejare Emmanuel and Olakunle Adeyemi Obasoro

**Mentor:** Elinah Moyo

**Project:** **Explore the project on GitHub**

AI systems process text using tokenisers, which break words and other text into smaller units that models can work with. But tokenisation methods developed primarily around English and other well-resourced languages may not handle the structure of African languages efficiently.

For languages with rich morphology, where words can contain multiple meaningful parts, a word may be split into many small pieces. According to Team Bangweulu, this can increase token counts, computational costs and processing time while potentially affecting how meaning is represented.

The team developed a morphologically aware SuperBPE approach aimed at improving tokenisation efficiency across more than 30 African languages.

Their motivation went beyond reducing the number of tokens. They wanted to address what they see as an infrastructure gap in AI development: African languages should not be disadvantaged simply because the tools used to process them were not designed with their linguistic characteristics in mind.

### The challenge behind the model

One of the team's biggest difficulties was sourcing and balancing datasets for languages that are not equally represented in available data.

To address this, the team grouped languages into typological categories and used shuffled sampling. It also capped samples from other groups to match the size of the smallest dataset, an approach intended to reduce imbalance and prevent some languages from disproportionately influencing vocabulary allocation.

The AI Research Foundation Course 1-4 helped the team build its technical understanding of tokenisation and embeddings. Wiam also highlighted the value of data cards and impact statements in thinking through the relationship between technical performance and societal impact.

### What winning meant

For Wiam, the announcement brought a mixture of joy, emotion and pride after the team's late nights and technical adjustments.

> “Winning validated every late night, every technical pivot, and our team's shared dedication to building meaningful infrastructure for African languages.”

The team does not intend to stop at tokenisation benchmarks. Its next step is to integrate the tokenizer into an active large language model pipeline and evaluate how it affects downstream text generation, training efficiency and reasoning.

That next phase will be important for determining whether improvements in tokenisation translate into meaningful gains in real AI applications.

Wiam's advice to other builders is to remain resilient and test their assumptions rigorously. Progress, in research, often comes from discovering that an initial approach can be improved.

## Team Atbara: Making Financial Complaint Analysis More Context-Aware

![Team Atbara](/uploads/1001242916.jpg "Team Atbara")

**Team lead:** Justina Odoeze

**Team members:** Nzube Ohalete, Sheree Edmund, Faith Kasunga and Sheila Nalweyiso

**Project:** **[Explore the project on GitHub](https://github.com/Elocodes/C10-team-atbara)**

As digital payments and cross-border commerce grow, financial institutions and payment providers must deal with large volumes of customer complaints. Understanding those complaints is not always straightforward, particularly when customers use local expressions, informal language or a mixture of languages.

Team Atbara is investigating this challenge through an AI approach to financial complaint analysis.

The team identified a limitation in existing customer-service systems: tools built around standard English or rigid keyword rules may struggle to interpret expressions in Nigerian Pidgin, Kenyan Sheng and other forms of local communication. Complaints may also refer to different payment systems and country-specific financial services.

When a system misunderstands a complaint, the consequences can include incorrect routing, delays in resolving customer problems and missed opportunities to identify issues that need urgent attention.

### Learning to define the problem carefully

The team's motivation came partly from personal experiences with customer-service systems that did not understand what people were trying to communicate or routed complaints incorrectly.

During development, one of the biggest challenges was agreeing on how to label complaints consistently.

For example, a complaint about food arriving cold after a late delivery could reasonably be interpreted as a product-quality problem or a delivery problem. If team members apply different interpretations to similar examples, the resulting training data can become inconsistent.

The team responded by consolidating its labelling rules, using AI to apply those rules more consistently, and introducing an “unclear” category for ambiguous complaints. Those unclear examples were excluded from training.

For Justina, this process reinforced an important lesson: model development begins long before training. The quality of the labels and the decisions made during data preparation can influence what a model learns.

She also credited the course's lessons on problem statements and data ethics with helping the team think more carefully about the problem it wanted to solve and the way it handled data.

### A result that means more than a placement

Justina recalls screaming with joy when the team was announced as one of the winners. The recognition felt like a reward for the team's weekly meetings, planning, deadlines and collaboration.

It also strengthened her confidence in her place in AI research.

> “This recognition strengthened my confidence that I belong in the research community and have something meaningful to contribute to shaping the future of AI in Africa.”

The team plans to strengthen its research and work towards publishing its findings.

For other African AI learners, Justina recommends starting with a specific problem that matters to the community, understanding it before building a model, and paying attention to data quality and ethics. She also encourages learners to collaborate, stretch beyond what they already know and work towards making their projects useful beyond a notebook.

Her message is a practical one: understanding the problem properly is as important as choosing the model.

## Team Chamo: Exploring Lightweight AI for Mental Health Support

![Team Chamo ](/uploads/1001242917.jpg "Team Chamo ")

**Team lead:** Bruno Nwagbo

**Team members:** Daniel Ohachor, Bassey Emmanuel Francis and Ademola James Aderemi

**Mentor:** Odion Joel Okonofua

**Project:** **[Explore the project on GitHub](https://github.com/iamcbn/C10-team-chamo)**

Access to mental health care remains a serious challenge in many African communities. Shortages of mental health professionals, geographical barriers and social stigma can make it difficult for people to seek support or receive timely assessment.

Team Chamo is exploring whether AI can help identify potential signs of mental health distress in everyday text communication, including messages and online conversations.

The idea is rooted in the possibility that people may express distress informally before they reach a healthcare professional. The team's goal is to investigate a resource-efficient approach that could support early identification, particularly in settings where computing resources and access to professional care are limited.

Importantly, a text-based model cannot independently diagnose a mental health condition. Any real-world application would need careful evaluation and appropriate clinical oversight.

### Distinguishing distress from everyday emotions

One of the team's biggest technical challenges was reducing the risk of the model interpreting ordinary negative emotions as signs of clinical distress while keeping inference lightweight.

A sad, fearful or angry statement does not necessarily indicate a mental health condition. A model that confuses these everyday emotions with clinical distress could produce misleading results.

To address this, the team augmented its dataset of 52,681 mental health statements with 30,000 additional “hard negative” statements. These included examples expressing sadness, fear and anger that were labelled as non-distress.

The aim was to help the model distinguish negative emotional language from the patterns it was designed to identify.

Bruno said that technical modules covering representation learning, regularisation and rigorous model evaluation informed the team's approach to probing the model and tuning its hyperparameters.

### From a research project to responsible application

Bruno described feeling happy, humbled and proud when the team was announced as a winner. He had not expected the team to finish among the top three, making the recognition particularly meaningful after weeks of experimentation, dataset curation and teamwork.

His next steps focus not only on adapting the project into a possible product, but also on making sure it is used responsibly.

The team hopes to improve its handling of Nigerian linguistic nuances, including Pidgin and local languages, and work with mental health practitioners to assess the model's accuracy.

Bruno is also conscious of the risk that mental health technology could be misused.

He wants the project to be developed ethically and used for good, rather than for stereotyping or profiling people. That concern is especially important for tools that interpret sensitive information about people's emotional states.

His advice to other African AI builders is to focus on genuine community problems and not let limited computing resources discourage them.

Thoughtful problem framing and data engineering, he argues, can matter more than simply using greater computing power or fine-tuning larger models. He also encourages builders to prioritise ethics and real-world usability from the beginning, remain consistent and trust their teams and mentors.

**Congratulations to Team Bangweulu, Team Atbara and Team Chamo on their achievements at TRI AI Cohort 10 Demo Day.**
