# Hugging Face Showcase

## Overview
Welcome to my open-source AI portfolio. This repository serves as a central hub for the models, datasets, and data engineering pipelines I have published on Hugging Face. My work primarily focuses on LLM, SLM, MLM, and Agentic AI, specifically for low-resource languages, and the architecture behind agentic workflows and models.

## BIRD-D&C-Instruct: Divide-and-Conquer Text-to-SQL
This dataset is designed to enhance the reasoning capabilities of Large Language Models (LLMs) in complex Text-to-SQL generation tasks. Built upon the challenging BIRD benchmark, it introduces a "Divide and Conquer" strategy for instruction tuning. Instead of forcing the model to generate highly complex, nested SQL queries in a single shot, the data is structured to teach the model how to break down intricate user requests into smaller, logical sub-problems. This step-by-step reasoning approach significantly improves the model's structural understanding of complex enterprise databases and relational schemas.

### Key Highlights
  - Divide & Conquer Reasoning: Structures training data to teach models how to decompose complex queries into manageable, logical steps, leading to highly accurate and executable SQL outputs.
  - Smarter Schema-Linking: After fine-tuning the model using this dataset, the model will learn how to select the correct tables and columns without extra schema-linking step.
  - BIRD Benchmark Integration: Leverages the complexity of the BIRD benchmark—one of the most demanding and realistic Text-to-SQL datasets—to simulate real-world, large-scale database environments.
  - Optimized for Instruction-Tuning: Carefully curated in a standardized prompt-response format, making it ideal for fine-tuning base LLMs for advanced schema linking and SQL generation.
  - Hallucination Mitigation: Significantly reduces the generation of invalid queries or incorrect JOIN operations by guiding the model through a transparent, sequential reasoning process.
  - Enterprise-Grade Schema Focus: Tailored to handle complex, real-world schemas that require a deep computational understanding of structural relationships, such as primary and foreign key constraints.

### Links:
  Dataset:
  - https://huggingface.co/datasets/BDanial/Instruct_bird_to_divide_and_conquer_tagged
  - https://huggingface.co/datasets/BDanial/Instruct_bird_to_divide_and_conquer

Proof of Concept Model (fine-tuned for 1 epoch using LORA method):
  - https://huggingface.co/BDanial/Granite-3.3-8b-instruct-bird-d-and-c


## d-asr-1 (Available upon request)
This dataset is a large-scale, comprehensive collection of Persian speech designed to significantly advance Automatic Speech Recognition (ASR) capabilities for the Persian language. Comprising approximately 100 hours of precisely aligned audio and text pairs, the dataset is uniquely grounded in the rich literary heritage. It features texts, vocabulary, and linguistic nuances spanning multiple centuries of Persian literature. Carefully processed and segmented into highly optimized ~4-second chunks, d-asr-1 is accompanied by rich metadata, making it an exceptional resource for training and fine-tuning robust ASR models on complex, domain-specific, or historical Persian language tasks.

### Key Highlights
  - Extensive Audio Corpus: Features ~100 hours of high-quality, accurately transcribed Persian speech, providing a substantial foundation for deep learning and acoustic modeling.
  - Optimized Chunking Strategy: All audio files are strictly segmented into ~4-second duration chunks. This ensures optimal memory efficiency during audio decoding and seamless pipeline processing with tools like the Hugging Face datasets library.
  - Historical & Linguistic Diversity: Captures the evolution of the Persian language by incorporating texts and dialects from various centuries, offering a rare opportunity to train models on classical phrasing and diverse structural nuances.
  - Rich Metadata Integration: Includes extensive, well-structured metadata accompanying the audio pairs, enabling advanced data filtering, specific dialect isolation, and highly customized instruction-based training.
  - LM and Whisper Fine-Tuning Ready: Perfectly structured and formatted for fine-tuning state-of-the-art ASR architectures (such as Whisper), making it highly effective for developing specialized transcription tools for low-resource or historically complex Persian audio.

### Link
  - https://huggingface.co/datasets/BDanial/d-asr-1

## PerMedCQA (Contributed)
PerMedCQA is the first large-scale, comprehensive Persian-language benchmark specifically designed for Consumer Question Answering (CQA) in the medical domain. Sourced from authentic, real-world interactions across prominent online healthcare forums, this dataset bridges a critical gap in low-resource multilingual medical AI. It contains over 68,000 highly refined question-answer pairs that reflect genuine patient inquiries and concerns. Crucially, the dataset is grounded in medical accuracy; the responses were originally provided by licensed physicians and subsequently double-checked and validated by professional doctors and expert human annotators to ensure the highest standards of clinical safety and factual reliability.

### Key Highlights
  - First Persian Medical CQA Benchmark: Serves as a pioneering, foundational dataset for evaluating and training Large Language Models (LLMs) on consumer-oriented medical inquiries in the Persian language.
  - Massive Scale & Authenticity: Comprises 68,138 carefully curated QA pairs (refined from over 87,000 raw entries) representing real-world, conversational patient-doctor interactions rather than artificial exam-style questions.
  - Expert Medical Validation: All answers within the dataset have been rigorously double-checked and validated by professional doctors. This guarantees clinical accuracy, making it a safe and highly reliable resource for healthcare AI development.
  - Rich Categorization & Metadata: The dataset spans a wide range of medical specialties and includes valuable metadata (such as patient demographics and physician specialty), allowing for highly contextualized instruction-tuning and personalized healthcare AI research.
  - Evaluated with MedJudge Framework: The data is optimized for modern evaluation frameworks, explicitly supporting rubric-based assessment of LLMs regarding their empathy, accuracy, and clinical reasoning in patient-facing applications.

### Link
  - https://huggingface.co/datasets/NaghmehAI/PerMedCQA

## LPRGHC Test-Set (Literatures - Politics - Religions - Geography - History - Cultural) (Contributed)
This dataset represents a significant paradigm shift in evaluating Large Language Models (LLMs) for the Persian language. While traditional benchmarks focus almost exclusively on linguistic proficiency, grammar, or translation capabilities, LPRGHC is pioneering as the first evaluation set explicitly designed to test an AI's deep understanding of a specific country's regional and cultural knowledge. Containing 12,362 carefully curated multiple-choice samples, this dataset evaluates whether a model truly comprehends the region's unique context. It challenges the assumption that speaking a language equates to understanding its people, proving that authentic localization requires a deep grasp of local history, religious nuances, literature, political structures, and geography.

## Key Highlights
  - Massive & Diverse Data Pool: The test set includes exactly 12,362 evaluation samples.
  - Beyond Linguistic Syntax: It sets a new standard for AI localization by shifting the evaluation focus from mere language syntax and translation to authentic cultural, historical, and regional awareness.
  - Comprehensive Macro-Categories: The data is systematically structured into 6 primary domains: History (4,442 samples), Religion (3,065 samples), Literature (2,223 samples), Politics (1,166 samples), Geography (978 samples), and Culture (488 samples).
  - Highly Granular Sub-Categories: The dataset is further broken down into 122 highly specific sub-categories. These cover intricate local knowledge, including Iranian history (both pre- and post-Islam), Persian proverbs and literature, the Iranian constitution, traditional Iranian-Islamic medicine, and detailed geographical queries spanning various provinces such as East Azerbaijan, Isfahan, and Khorasan.
  - Crucial for Real-World Deployment: Essential for evaluating models intended for local administrative, educational, or commercial use, ensuring they possess the factual baseline required to interact intelligently within a specific cultural framework and avoid contextual hallucinations.
## Link
  - https://huggingface.co/datasets/UT-NLP-LAP/LPRGHC

## APARSIN/persian-dialects-pretraining (Contributed)
Created by the APARSIN (SilkRoadAparsin) organization, this comprehensive pretraining corpus is specifically engineered to address the severe data scarcity in __extremely low-resource_ Persian dialects and related regional languages. By carefully aggregating, normalizing, and categorizing text from highly sparse and disparate sources, this dataset provides a robust foundation for pretraining Large Language Models (LLMs) on underrepresented linguistic groups. Maintained as a gated dataset to ensure data integrity and responsible usage, it is a critical resource for preserving regional languages and advancing inclusive multilingual AI.

### Key Highlights
  - Focus on Underrepresented Dialects: Exclusively targets extremely low-resource languages and dialects, including Hazaragi, Dari, Gilaki, Pashto, and diverse Kurdish dialects (Central/Sorani, Northern/Kurmanji, Southern), alongside Standard Persian for alignment.
  - Large-Scale Data Aggregation: Consolidates and standardizes sparse data from a wide variety of fragmented sources (e.g., Hezarai, Arman, Parsinlu, DOLMA, PEYMA, BBC) into a unified pretraining pipeline.
  - Conflict-Free Schema Architecture: Designed with a robust structure to prevent schema conflicts during massive data loading. All source-specific metadata is safely preserved within a JSON-serialized extra field, ensuring seamless integration with the Hugging Face datasets library.
  - Optimized for LLM Pretraining: Structured specifically for the pretraining phase of foundational models, providing the raw, categorized textual volume necessary for models to learn the deep syntactic and semantic nuances of these localized dialects.
    
### Link
  - https://huggingface.co/datasets/APARSIN/persian-dialects-pretraining
