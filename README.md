# RAG Knowledge Search

Retrieval-augmented generation (RAG) over company documents, so answers come from your own SOPs and records instead of guesses. Every answer points back to the document it came from.

> The source code is not public. This repository documents how the system works. A live walkthrough is available on request.

## The problem

SOPs, policies and process documents were spread across folders. Staff asked colleagues instead of reading them, and answers varied from person to person.

## Features

- Documents are split into **searchable chunks** and stored as embeddings
- For each question, the system **finds the most relevant passages** with vector search
- An LLM writes the answer **using only those passages**
- Each answer **names the source document**, for example SOP.pdf or Policy.docx

## How it works

```
Ingest:  SOPs / policies / records  ->  split into chunks  ->  embeddings  ->  vector index

Ask:     question  ->  embedding  ->  top matching chunks  ->  LLM  ->  answer + sources
```

## Tech stack

Python, RAG, embeddings, vector search, LLMs (OpenAI and Gemini APIs)

## My role

I built the ingestion pipeline, the retrieval step and the answer format with sources.

## Related

- [LLM business assistant](https://github.com/mrsaurabhkumarsharma/llm-business-assistant)
- [LangChain document Q&A](https://github.com/mrsaurabhkumarsharma/langchain-document-qa)

## Author

**Saurabh Kumar Sharma**, Automation Specialist  
[Portfolio](https://mrsaurabhkumarsharma.github.io) · [LinkedIn](https://www.linkedin.com/in/saurabh-sharma-7aa432416) · mrsaurabhkumarsharma@gmail.com
