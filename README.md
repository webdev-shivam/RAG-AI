# RAG Pipeline Development Task

## Overview

Build a Retrieval-Augmented Generation (RAG) pipeline that can answer questions about BrewGenius coffee/espresso machine products using the provided product knowledge base.

---

## Objective

Create a working RAG pipeline that:
1. Ingests the provided product documentation
2. Retrieves relevant context for user queries
3. Generates accurate, grounded responses using an LLM
4. Optimizes for accuracy, latency, and token efficiency

---

## Provided Resources

- `data/BrewGenius_Product_Guide.md` - Complete product knowledge base (your source document)

**That's it.** You are responsible for all architecture decisions, tool selection, and implementation.

---

## Requirements

### Functional Requirements

Your pipeline must:

1. **Ingest** the product guide and prepare it for retrieval
2. **Retrieve** relevant document chunks based on user queries
3. **Generate** answers using an LLM with retrieved context
4. **Handle** various question types:
   - Product specifications (e.g., "What is the water tank capacity of ProBarista Elite?")
   - Comparisons (e.g., "Compare ProBarista Elite vs Studio")
   - Recommendations (e.g., "Which machine is best for a small apartment?")
   - Troubleshooting (e.g., "My espresso is bitter, what should I do?")
   - Pricing and availability (e.g., "What's the cheapest espresso machine?")
   - General knowledge (e.g., "What grind size should I use for pour over?")

### Non-Functional Requirements

Optimize for:

**Accuracy**
- **Target:** Answers must be factually correct based on source document
- **Why It Matters:** User trust

**Latency**
- **Target:** Response time should be reasonable for interactive use
- **Why It Matters:** User experience

**Token Efficiency**
- **Target:** Minimize tokens sent to LLM while maintaining accuracy
- **Why It Matters:** Cost reduction

---

## Evaluation Criteria

Your submission will be evaluated on:

### 1. Architecture Design (25%)
- Document chunking strategy and rationale
- Embedding model selection and justification
- Vector store choice
- Retrieval mechanism design
- Prompt engineering approach

### 2. Implementation Quality (25%)
- Code organization and clarity
- Error handling
- Configurability
- Documentation

### 3. Performance Metrics (30%)
- Answer accuracy on test queries
- Retrieval relevance (are the right chunks being retrieved?)
- Response latency
- Token usage per query

### 4. Optimization Techniques (20%)
- Techniques used to improve accuracy
- Techniques used to reduce latency
- Techniques used to minimize token consumption
- Trade-off analysis and decisions

---

## Test Queries

Your pipeline will be tested against queries including (but not limited to):

```
1. "What is the price of the ProBarista Elite?"
2. "Which coffee maker has a built-in grinder?"
3. "How do I fix weak espresso?"
4. "Compare the SmartBrew Pro 12 and SmartBrew Pro 8"
5. "What's the warranty on the grinder burrs?"
6. "I have a small kitchen - which machine do you recommend?"
7. "What grind setting should I use for French Press on the GrindMaster Pro?"
8. "Does the ProBarista Compact have a dual boiler?"
9. "What water hardness is recommended?"
10. "How often should I descale my machine?"
```

---

## Deliverables

Submit the following:

### 1. Source Code
- Complete, runnable pipeline code
- Setup instructions (dependencies, API keys, etc.)
- Example usage script

### 2. Architecture Document
A brief document (1-2 pages) explaining:
- Your architecture choices and why
- Chunking strategy
- Embedding model selected and why
- Retrieval approach (k value, reranking, etc.)
- Prompt design
- Any optimization techniques applied

### 3. Performance Report
Include metrics for:
- Average response latency
- Average tokens per query (input + output)
- Accuracy on test queries (self-evaluated)
- Retrieval quality observations

---

## Constraints

- **No access to this codebase** - Build everything from scratch
- **LLM of your choice** - OpenAI, Anthropic, local models, etc.
- **Any programming language** - Python recommended but not required
- **Any libraries/frameworks** - LangChain, LlamaIndex, custom implementation, etc.
- **Internet access allowed** - Research best practices, techniques, documentation

---

## Getting Started (Suggested)

This is just a suggestion - you may approach this differently:

1. **Research Phase**
   - Study RAG architectures and best practices
   - Understand chunking strategies
   - Learn about embedding models and vector stores

2. **Design Phase**
   - Plan your architecture
   - Make technology choices
   - Design your prompts

3. **Implementation Phase**
   - Build the ingestion pipeline
   - Implement retrieval mechanism
   - Integrate LLM generation
   - Add optimizations

4. **Evaluation Phase**
   - Test with provided queries
   - Measure performance metrics
   - Iterate and improve

---

## Submission

Submit your completed work including:
- [ ] Source code (GitHub repo or zip file)
- [ ] Architecture document (PDF or Markdown)
- [ ] Performance report (PDF or Markdown)
- [ ] Working demo or video walkthrough

---

*Good luck! Focus on understanding the fundamentals - the best solutions come from deep understanding, not just copying code.*
