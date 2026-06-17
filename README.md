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

### Links
  - https://huggingface.co/datasets/BDanial/d-asr-1

