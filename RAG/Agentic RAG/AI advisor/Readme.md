# Agentic RAG for portfolio & tax management

This project is an intelligent Robo Advisor that combines finance, data engineering, and modern AI to create a multi-capability system for:

- Managing and analyzing investment portfolios  
- Generating professional, actionable investment insights  
- Answering tax-related questions using grounded RAG


## What it does

### 1. Portfolio management
- Users create and update portfolios with asset names, units, and average cost.
- Data is stored persistently in JSON for each user.
- Input is validated and normalized to prevent invalid states.

### 2. Portfolio analysis
- Fetches live and historical market data using 'yfinance'.
- Computes:
  - Current value & gain/loss  
  - Expected returns  
  - Covariance matrix (risk relationships)  
- Applies principles from Modern Portfolio Theory.
- Uses an LLM as a portfolio manager agent to generate actionable insights.

### 3. Tax consultation RAG
- Loads and chunks tax law documents (Germany and US documents attached).
- Builds a hybrid retrieval system:
  - BM25 (lexical precision)
  - FAISS + embeddings (semantic understanding)
- Combines both using an ensemble retriever.
- Grounds LLM responses in retrieved legal text.

---

This project demonstrates how retrieval, computation, and language models can be combined into a production-style AI architecture for real financial and legal use cases.

