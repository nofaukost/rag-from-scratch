# RAG from Scratch 🔍

Building Retrieval-Augmented Generation (RAG) pipelines from the ground up. Learn how to combine Large Language Models with external knowledge bases for accurate, grounded AI responses.

## What is RAG?

RAG enhances LLM responses by retrieving relevant documents from a knowledge base before generating answers, reducing hallucinations and enabling domain-specific Q&A.

## Architecture

```
                    ┌─────────────────┐
                    │   User Query    │
                    └────────┬────────┘
                             │
                    ┌────────▼────────┐
                    │   Embedding     │
                    │   Model         │
                    └────────┬────────┘
                             │
              ┌──────────────▼──────────────┐
              │      Vector Database        │
              │   (Similarity Search)       │
              └──────────────┬──────────────┘
                             │
                    ┌────────▼────────┐
                    │  Top-K Relevant │
                    │  Documents      │
                    └────────┬────────┘
                             │
              ┌──────────────▼──────────────┐
              │     LLM + Context           │
              │  (Generate Answer)          │
              └──────────────┬──────────────┘
                             │
                    ┌────────▼────────┐
                    │  Grounded       │
                    │  Response       │
                    └─────────────────┘
```

## Key Concepts Covered

- **Document Loading** — Ingesting data from various sources
- **Text Splitting** — Chunking strategies for optimal retrieval
- **Embeddings** — Converting text to vector representations
- **Vector Stores** — Storing and searching document embeddings
- **Retrieval Chains** — Combining retrieval with LLM generation
- **Prompt Engineering** — Crafting prompts for grounded responses

## Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white)

## Getting Started

```bash
git clone https://github.com/nofaukost/rag-from-scratch.git
cd rag-from-scratch
pip install langchain openai chromadb tiktoken
export OPENAI_API_KEY=your_key_here
```

## License

MIT
