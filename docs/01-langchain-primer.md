# RAG Frameworks Primer

### (LangChain, LangGraph, LangSmith)

This short guide helps you understand the **core frameworks** used to build modern Retrieval-Augmented Generation (RAG) systems—especially as you move toward **enterprise-grade architectures**.

---

# 1. What Are We Building?

We are building a **RAG application** that evolves into an **enterprise-ready system** with:

- Hybrid Retrieval (**BM25 + Vector Search**)
- Cross-Encoder Reranking
- Citation Enforcement
- CI-Gated Evaluation Pipeline

---

# 2. The Three Core Frameworks

## LangChain — The Builder (Toolbox)

LangChain provides the **building blocks** for LLM applications.

Use it for:

- Loading documents
- Chunking text
- Generating embeddings
- Storing vectors
- Retrieving context
- Prompting LLMs

👉 Think of it as: **"How do I build a RAG pipeline?"**

---

## LangGraph — The Orchestrator (Workflow Engine)

LangGraph controls **how your system behaves across multiple steps**.

Use it when you need:

- Conditional logic (if/else)
- Multi-step workflows
- Query rewriting loops
- Multi-agent coordination
- Stateful execution

👉 Think of it as: **"What happens next in my AI system?"**

---

## LangSmith — The Observer (Debugging + Evaluation)

LangSmith helps you **see, debug, and improve** your system.

Use it for:

- Tracing execution
- Debugging prompts
- Evaluating outputs
- Monitoring latency and cost

👉 Think of it as: **"Why did my system produce this answer?"**

---

# 3. How They Work Together

```text
LangChain   → Builds the pipeline
LangGraph   → Controls the workflow
LangSmith   → Observes and evaluates
```

---

# 4. When to Use What

## Simple RAG (Start Here)

Use:

- LangChain

Flow:

```text
User → Retriever → LLM → Answer
```

---

## Production RAG

Use:

- LangChain + LangSmith

Adds:

- Debugging
- Evaluation
- Observability

---

## Enterprise RAG (Target State)

Use:

- LangChain + LangGraph + LangSmith

Adds:

- Hybrid retrieval
- Reranking
- Multi-step reasoning
- Workflow orchestration
- Evaluation pipelines

---

# 5. Key Enterprise Concepts (Preview)

## Hybrid Retrieval

Combine:

- BM25 (keyword search)
- Vector search (semantic search)

Goal: Improve recall and precision.

---

## Cross-Encoder Reranking

Re-score retrieved documents using a **more accurate (but slower) model**.

Goal: Improve ranking quality.

---

## Citation Enforcement

Force the model to:

- Ground answers in retrieved documents
- Provide references

Goal: Reduce hallucinations.

---