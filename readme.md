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

> Anthropic AI refers to the artificial intelligence research and development group that is part of OpenAI. It was founded by Elon Musk, Sam Altman, and other prominent figures...

**Observation:** The base model produced incorrect claims, including that Anthropic is part of OpenAI and was founded by Elon Musk and Sam Altman.

### Qwen with RAG

> Anthropic AI is an American artificial intelligence (AI) public benefit corporation headquartered in San Francisco, California. Its flagship product is Claude, a series of proprietary large language models (LLMs)...

**Observation:** With retrieved context from the knowledge database, the model provided a substantially more accurate description of Anthropic, including its location and flagship product.

### Takeaway

This example demonstrates how Retrieval-Augmented Generation (RAG) can reduce hallucinations by grounding model responses in retrieved information. RAG does not guarantee factual accuracy, and the quality of its answers still depends on retrieval relevance and the model's use of the provided context.


## Notebooks

* `Data_Collection.ipynb` — Collects Wikipedia data on Anthropic, Jev (AI model), Grok, GPT-6, and Claude Mythos.
* `Base_vs_Rag_Inference.ipynb` — Tests and compares the base model's responses with RAG-based responses.

## Tech Stack

Python · ChromaDB · Unsloth · Wikipedia-API

## Goal

Explore how retrieval-augmented generation can improve factual grounding and answer quality compared with a base language model.
