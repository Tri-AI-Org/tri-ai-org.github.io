---
title: "Where AI Meets Real Problems: The Nine TRI AI Cohort 10 Finalists "
date: 2026-09-30
division: teaching
excerpt: "Where AI Meets Real Problems: The Nine TRI AI Cohort 10 Finalists"
draft: false
---
What happens when a community of AI learners moves beyond learning concepts and starts building solutions to problems that matter to them? TRI AI Cohort 10 put its learning into practice through nine ambitious capstone projects, exploring how Small Language Models (SLMs), natural language processing, and retrieval augmented generation can be used to tackle real-world challenges. 

Here are the projects representing the nine capstone tracks.

**Team Kinyeti: Making Agricultural Knowledge Easier to Find** 

A farmer notices something is wrong with their maize. The leaves have holes, and the cobs are smaller than expected. They need an answer, but finding the right agricultural advice is not always straightforward. The information may already exist, buried somewhere among hundreds of agricultural advisory documents written for different crops, countries, and farming conditions. The challenge is knowing where to look and finding the information that is actually relevant.


That is the problem Team Kinyeti set out to address with Agricultural Extension RAG, a system designed to make agricultural knowledge easier to search and retrieve. The system takes a farming question written in plain language and searches through a collection of 695 agricultural advisory texts covering 13 crops across 21 African countries, returning the five documents it considers most relevant.


To improve how those documents are found and ranked, the team experimented with both semantic and keyword based retrieval. They fine tuned a BGE bi encoder for semantic matching and used a BGE cross encoder to rerank the results. Their final hybrid pipeline combined BM25 keyword search, dense retrieval, and reranking, achieving an nDCG@5 score of 0.93753 on the private leaderboard and placing the team third overall.


The team also wanted users to see what happens behind the scenes. They built an interactive demonstration that allows users to compare different retrieval approaches and follow how documents move through the retrieval pipeline. Rather than simply presenting a list of results, the system provides a clearer view of how those documents were identified and ranked.


At the same time, Kinyeti recognizes the limitations of the current prototype. The document collection is primarily in English and often uses technical agricultural language, so the system is not intended to replace agricultural extension officers or independently determine what a farmer should do. Instead, the project provides a foundation that could be expanded with more local language resources, broader agricultural data, and feedback from agricultural extension professionals.
Explore the project: [Kinyeti Link](< https://overwatch886sociot--team-kinyeti-rag-ui.modal.run/>)
Team: Israel Olawuyi Mobolaji · Harry Okah · Edike Jeremiah · Chisom Okafor
Mentors: Oluwaseun Ajayi · Samuel Taiwo · Adnan Adetunji

**Team Atbara: Building AI for African Customer Complaints**

A customer reports a failed transfer in Nigerian Pidgin. Another describes a delivery problem in Kenyan Sheng. To a human customer service agent, the meaning may be clear from context. But for automated support systems trained primarily on standardized English, complaints expressed in local languages and dialects can be much harder to interpret accurately. 


Team Atbara set out to address this challenge with their project, Intelligent Complaint Classification Using Localized Transformer Architectures. They developed a fine tuned DeBERTa v3 model designed to classify customer complaints into 10 operational categories while also assigning priority levels. The model was trained on 14,499 complaints, including anonymized reviews from users across Nigeria, Ghana, Kenya, and South Africa.


The dataset represented a range of real world customer experiences, covering services and platforms such as Jumia, Shein, Kilimall, Takealot, Temu, Glovo, Bolt Food, and Checkers Sixty60. However, Atbara’s approach went beyond simply asking whether the model could classify a complaint correctly. The team also considered what should happen when the model is not confident in its prediction. Using a confidence threshold, the system can identify uncertain cases and route them to a human agent rather than processing them automatically. This becomes particularly important for financially sensitive complaints, where an incorrect classification could have serious consequences. The team also used inverse class weighting to give greater attention to less frequent but potentially serious categories, including unauthorized fraud.


The project also considers the broader implications of deploying AI in customer support. Alongside the model, Atbara developed a data card, impact statement, and stakeholder engagement plan that examined issues such as language bias, automation bias, and the risks of incorrectly handling sensitive complaints.
In the end, the project asks a question that extends beyond model accuracy: Can an AI system understand a complaint, and can it also recognize when a human should take over?
For Team Atbara, building a useful customer support system means addressing both sides of that question.
Explore the project: [Atbara Github Link](https://github.com/Elocodes/C10-team-atbara)

![](/uploads/screenshot-2026-09-30-200018.png "Team: Justina Odoeze, Sheree Edmund, Nzube Ohalete, Faith Kasunga, Sheila Nalweyiso")

**Team Bwindi: Bringing Climate Aware Pest Management Closer to Farmers** 

![](/uploads/crawlm-prototype-1-.png)

A farmer growing maize, rice, or sorghum may know that pests are affecting their crops, but finding reliable information about what to do next can be difficult. Advice on pest management and the effects of changing climate conditions is often scattered across research papers, agricultural extension manuals, government publications, and agro advisory platforms. Much of this information is also written for technical audiences rather than the farmers who need it most.

Team Bwindi approached this challenge by building CrawLM, the Climate Responsive Agricultural Wizard Language Model, a lightweight small language model designed to provide accessible information about climate aware pest management for staple cereal crops across West Africa. The team focused on maize, rice, and sorghum, developing a system that brings information from a range of agricultural and scientific resources into a more accessible format. Their data was sourced from regional and global repositories including FAO AGRIS, the CABI Plantwise Knowledge Bank, GBIF, and NASA, among others.

Under the hood, CrawLM is built on Meta’s Llama 3.2 3B Instruct model and was fine tuned for the target agricultural domain using QLoRA. The model can respond to questions about pest management in growing and stored cereal crops, as well as questions about how climatic conditions can affect crop development. The team evaluated the model from both quantitative and qualitative perspectives. Its final validation loss was 2.0209, while additional evaluation focused on domain specific edge cases to examine how the model responds to agricultural questions that may require more nuanced understanding.

The result is a lightweight agricultural AI tool designed to put relevant information into a format that is easier to access and use. Rather than requiring farmers to navigate multiple technical repositories, CrawLM aims to bring a more concentrated source of climate and pest management knowledge into a single interface.
The prototype is currently available through Hugging Face Spaces, where users can interact directly with the model.
Explore the project: [CrawLM Link](https://huggingface.co/spaces/zerothvictor/CrawLM-Playground)



**Team Binga: Preserving African Folktales Through AI** 

![](/uploads/screenshot-2026-09-18-142226.png)

African folktales have traditionally been passed down through generations through oral storytelling. However, many culturally significant stories and the knowledge they carry remain underrepresented and difficult to access in digital spaces. Team Binga set out to explore how artificial intelligence could help preserve and improve access to these storytelling traditions.

The team developed a domain specific Small Language Model focused on African folktales, using a curated dataset of stories to explore how lightweight AI could work with culturally specific content. Their project combined document retrieval with model fine tuning, allowing them to explore different ways of identifying and working with relevant folktales based on user prompts. Beyond building the technology, the project also encouraged the team to consider important questions around the responsible use of AI for cultural knowledge, including cultural representation, authenticity, bias, copyright, and the role of communities in preserving and sharing their traditions.
Project repository: [Binga Github Link](https://github.com/flexydave/C10-team-Binga)
Team: David Attah , Bright Francis , Orangun Folaranmi
Mentor: Patrick Owor



**Team Bangweulu: Rethinking How AI Processes African Languages**

![](/uploads/morphologically-aware-superbpe.png)

African languages present unique challenges for modern language models. Many have complex morphological structures, different writing systems, and linguistic characteristics that are not always well represented by the tools used to build today's AI systems. When standard tokenizers process African languages, words can be broken into unnecessarily small pieces, increasing the amount of text that models need to process and potentially affecting how efficiently they work.


Team Bangweulu set out to address this challenge by developing a morphologically aware SuperBPE tokenizer designed for more than 30 African languages. Their project focuses on an important part of AI infrastructure: how text is broken down into smaller units before it is processed by a language model.
The team designed their tokenizer to account for differences between African languages rather than treating all languages in the same way. Their approach uses a two stage process that identifies useful subword patterns and can also combine tokens across word boundaries when appropriate. They also adapted the tokenizer's vocabulary allocation to different types of languages, including agglutinative, fusional, and analytic languages.


The project evolved through several rounds of experimentation. Early prototypes relied on different heuristics for identifying useful language patterns, but the team found that these approaches were not making the most efficient use of their vocabulary. They refined the system by reducing duplicated vocabulary entries, improving the way tokens were selected, and testing how different amounts of language data affected performance.
Their final system achieved 100% lossless round trip accuracy on their local benchmark and 100% exact accuracy on the competition evaluation set. The results demonstrated that the tokenizer could process the evaluated text while preserving the original content exactly.


For Team Bangweulu, the project represents more than an improvement to tokenization. It highlights the importance of building AI infrastructure that takes African languages into account from the ground up. By improving how African text is represented and processed, the team hopes to contribute to more efficient and accessible language technologies for African communities.
Project repository: [Bangweulu Github Link](https://github.com/AtfiWiam/C10-team-Bangweulu)
Core project team: Wiam Atfi and George Aladejana
Mentor: Elinah Moyo
Early collaborators: Adejare Adedayo and Obasoro Olakunle Adeyemi


**Team Simien: Helping Farmers Find the Right Agronomic Advice**

![](/uploads/02_problem.png)

![](/uploads/01_pipeline.png)

Smallholder farmers often need quick and specific answers when dealing with problems such as nutrient deficiencies, pest outbreaks, or crop diseases. However, much of the expert knowledge available to address these challenges is scattered across agricultural extension materials, making it difficult to identify the most relevant guidance when it is needed.


Team Simien, made up of Hamna Kaleem and Kamaya Ndigwa Esperance M., set out to address this challenge by improving how agricultural information is retrieved. Their project, Optimizing RAG Document Retrieval for Agronomic Advice, focuses on the retrieval component of a retrieval augmented generation system, helping connect farmers' questions with useful agricultural knowledge.


The team worked with 695 agricultural extension fact sheets covering crop diseases, pests, nutrient deficiencies, soil management, climate adaptation, and fertilizer advice. Rather than depending solely on keyword matching, the system looks at the intent behind a question and considers details such as the crop, the agricultural issue, the type of information being requested, and the agro ecological zone.
This approach is particularly important when similar symptoms can have different causes or require different recommendations. A question about why maize leaves are turning yellow, for example, may require a different document from a question asking how to prevent the problem. Team Simien's retrieval system is designed to distinguish between these types of requests and rank the documents that are most relevant to the question.


The system combines multiple retrieval and machine learning techniques to improve document ranking. The team evaluated the approach using cross validation and the nDCG@5 metric, comparing its performance with a baseline retrieval method. They also developed a reproducible end to end pipeline, making it possible for others to examine, test, and build on their work.


Beyond the technical system, the project highlights some of the practical challenges involved in developing AI for agriculture. Agricultural advice can vary depending on the agro ecological region, while existing knowledge bases may not adequately represent every farming community. Simien identified opportunities to involve farmers and agricultural extension professionals in future development, as well as improve support for multilingual and code switched queries.
Project Repository: [Simien Github Link](https://github.com/Hamna-Kaleem/C10-team-simien)
Team: Hamna Kaleem and Kamaya Ndigwa Esperance M.


**Team Nyriagongo: Teaching AI to Reveal What It Already Knows About Toxicity**


Team Nyriagongo explored whether a language model already contains a usable signal for detecting toxic content within its internal representations.
Online platforms and conversational AI systems need to identify abusive, threatening, and harassing content at a scale that manual review cannot easily handle. Traditional approaches such as keyword filters can also miss more subtle forms of hostility, while training a separate model for content moderation can require additional computing resources and produce systems that are difficult to interpret.
Team Nyriagongo, led by Blessings Mambwe alongside Fafemi Adeola, Musonda Musunga, and Hamna Kaleem, approached the problem from a different direction. Instead of building a larger toxicity classifier or fine tuning an entire language model, they wanted to find out whether a language model already contains information about toxicity that could be extracted with a much simpler method.
Their project, Latent Probing for Toxicity Detection, uses Google's Gemma 2 2B language model as a frozen model. The team kept all 2.6 billion parameters unchanged and examined the model's internal representations at a specific layer. They then trained a lightweight linear classifier, known as a probe, to determine whether the information contained in those representations could distinguish between toxic and non toxic content.
To test the idea, the team built a harmonised dataset containing 108,468 examples from 13 public sources. They developed the complete pipeline, from preparing the data and extracting the model's internal representations to training and validating the probe. Their evaluation also included leave one source out testing, allowing them to examine whether the approach could generalise beyond the individual datasets used to build it.
The results provided a strong signal that the approach was worth investigating further. The system achieved 89.76 percent accuracy on the CodaBench development set and 92.35 percent on the held out testing set, correctly classifying 1,256 of 1,360 test examples.
The result is not presented as a finished content moderation product. Instead, Team Nyriagongo sees the project as a research prototype for understanding what information may already be encoded within language models. A simple probe can provide a more transparent way to investigate a specific concept without changing the underlying model, while also making it easier to examine where the approach succeeds and where it fails.
The team also recognises the limitations of treating toxicity as a simple binary classification problem. Language can depend heavily on context, intent, quotation, counterspeech, and cultural differences. Their proposed safeguards include human review, subgroup evaluation, and monitoring for changes in performance over time rather than relying on the system for autonomous enforcement.
What makes Team Nyriagongo's project particularly interesting is the question behind it. Rather than assuming that solving a safety problem requires a bigger or more heavily trained model, the team investigated whether existing models already contain useful signals that can be accessed through simpler and more interpretable methods. Their Cohort 10 project offers one measured answer to that question and opens the door to further research into how safety related concepts are represented inside language models.
Project Repository: Nyiragongo Github Link
Team: Blessings Mambwe, Fafemi Adeola, Musonda Musunga, and Hamna Kaleem
Mentor: Moses
Team Karisimbi: Building a Medical AI Grounded in Nigerian Clinical Guidance
Team Karisimbi is developing a small language model for medical advice grounded in Nigerian clinical guidelines.
Healthcare workers and patients may need reliable medical information at the point of care, yet general purpose AI systems may not always provide information that is grounded in a country's clinical guidelines. Team Karisimbi is exploring how AI can be developed around local medical guidance, using the Nigeria Standard Treatment Guidelines (NSTG) as its initial foundation.
The team is building a lightweight medical AI pipeline that combines structured clinical knowledge from Nigerian treatment guidelines with retrieval augmented generation and efficient model fine tuning. The system is designed to retrieve relevant medical information and use it to generate concise responses to healthcare questions.
The project began through the Kaggle Medical Advice SLM Challenge, where Team Karisimbi developed an early prototype using Gemma 2 2B IT, LoRA fine tuning, and TF IDF retrieval. The prototype produced responses averaging approximately 50 characters, meeting the challenge's requirement for concise medical answers.
The team is now extending the prototype by incorporating Nigerian clinical guidance into the dataset and model development. The goal is to create a small and efficient system that can provide evidence grounded medical information relevant to the Nigerian healthcare context.
Responsible AI is also built into the project. Team Karisimbi has developed a Problem Statement, Data Card, Impact Statement, stakeholder map, and stakeholder engagement plan covering healthcare workers, patients, and community members. These materials address issues such as safety, privacy, fairness, transparency, inclusivity, and community well being.
The system is intended as a decision support tool rather than a replacement for qualified healthcare professionals. This keeps the project's focus on using AI to support access to relevant medical information while recognising the importance of professional judgment in healthcare.
The project demonstrates how small language models can be adapted to specific healthcare needs by combining efficient AI techniques with locally relevant clinical knowledge.
Project Repository: Karisimbi Github Link
Team: Kpokpe Favour Ogheneruese 
Team Chamo: Teaching AI to Tell the Difference Between Distress and Everyday Emotion
Team Chamo developed a low latency AI system designed to distinguish clinical distress from everyday expressions of negative emotion.
People regularly express frustration, sadness, anger, or stress without necessarily experiencing clinical psychological distress. Distinguishing between these everyday emotions and genuine signs of distress can be difficult for automated systems, particularly when they rely on simple keyword matching. In digital mental health platforms, this can lead to false positives and make it harder to identify cases that may require closer attention.
Team Chamo explored how AI could learn this distinction more effectively. Their goal was to develop a lightweight clinical distress classification system capable of identifying signals of psychological distress while remaining fast enough for practical use.
The team's prototype uses the internal representations of Gemma 2 2B, focusing on information extracted from one of the model's layers. On top of these representations, they built an ensemble of three lightweight neural networks that work together to classify whether a statement reflects clinical distress or everyday negative emotion.
One of the team's key challenges emerged from the data used to train the system. The initial model tended to favour distress predictions, making it more likely to classify ordinary negative emotional statements as clinical distress. To address this, the team introduced 30,000 hard negative examples representing everyday emotional expressions. These examples helped the model learn a clearer distinction between common emotional experiences and statements more strongly associated with psychological distress.
The team also focused on keeping the system fast. Rather than relying on heavier software frameworks during inference, they implemented the trained model using a lightweight NumPy based approach, allowing it to make predictions in approximately 0.23 seconds. The prototype achieved an accuracy of 0.9039, demonstrating that a relatively lightweight system could capture a useful signal from the language model's internal representations.
The project sits at the intersection of clinical AI triage and edge AI deployment, where speed and efficiency can be important alongside predictive performance. At the same time, a system designed to identify psychological distress requires careful consideration of how its predictions are used, particularly because emotional language can be highly dependent on context.
By focusing on the boundary between everyday negative emotion and clinical distress, Team Chamo is exploring how AI could support the identification of potentially important signals without treating every expression of frustration or sadness as a clinical concern. The project demonstrates how careful dataset design, lightweight modelling, and efficient deployment can come together to address a specific challenge in mental health AI.
Project Repository: Chamo Github Link
Team: Bruno Nwagbo, Daniel Ohachor, Bassey Emmanuel Francis, Ademola James Aderemi
