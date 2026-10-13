# RAG-Based Question Answering System

A Retrieval-Augmented Generation (RAG) project that enhances a language model's answers by retrieving relevant information from a ChromaDB vector database.

## Features

* Collects AI-related information from Wikipedia using `wikipediaapi`.
* Stores and retrieves relevant text chunks using ChromaDB.
* Compares base-model responses against RAG-enhanced responses.
* Topics used for info - Claude Mythos, GPT-6, Grok, Jev AI Model, Anthropic.

## Example: Base Model vs. RAG

**Question:** What is Anthropic AI?

### Base Qwen

> Anthropic AI refers to the artificial intelligence research and development group that is part of OpenAI. It was founded by Elon Musk, Sam Altman, and other prominent figures in the field of machine learning and artificial intelligence. The goal of Anthropic AI is to develop safe and beneficial AI systems that can help humans solve complex problems and improve our lives. They conduct research on various aspects of AI, such as ethics, safety, and policy, and work closely with industry partners to ensure that their research is applied in a responsible and effective way.

**Observation:** The base model produced incorrect claims, including that Anthropic is part of OpenAI and was founded by Elon Musk and Sam Altman.

### Qwen with RAG

> Anthropic AI is an American artificial intelligence (AI) public benefit corporation headquartered in San Francisco, California. Its flagship product is Claude, a series of proprietary large language models (LLMs). The company is privately held but reportedly plans an initial public offering in 2026. Anthropic is one of the world's most valuable AI pure play companies, rivaled by OpenAI.

**Observation:** With retrieved context from the knowledge database, the model provided a substantially more accurate description of Anthropic, including its location and flagship product.

### Takeaway

This example demonstrates how Retrieval-Augmented Generation (RAG) can reduce hallucinations by grounding model responses in retrieved information. RAG does not guarantee factual accuracy, and the quality of its answers still depends on retrieval relevance and the model's use of the provided context.

More Examples at `Examples.txt`


## Notebooks

* `Data_Collection.ipynb` — Collects Wikipedia data on Anthropic, Jev (AI model), Grok, GPT-6, and Claude Mythos.
* `Base_vs_Rag_Inference.ipynb` — Tests and compares the base model's responses with RAG-based responses.

## Tech Stack

Python · ChromaDB · Unsloth · Wikipedia-API

## Goal

Explore how retrieval-augmented generation can improve factual grounding and answer quality compared with a base language model.
