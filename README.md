# RAG Pipeline Development Task

## Time Limit: 90 Minutes

## Tools Allowed

You may use:
- **Internet** for research
- **AI tools** (ChatGPT, Claude, Copilot, etc.)
- **AI-powered editors** (Cursor, Windsurf, etc.)
- **Any libraries or frameworks**

**However:** Since AI tools are allowed, we expect HIGHER quality. We evaluate not just that your pipeline works, but that you UNDERSTAND it. Generic, copy-pasted solutions will score poorly.

---

## What You'll Build

A RAG pipeline that answers questions about BrewGenius coffee/espresso machine products using the provided product knowledge base.

**Provided:**
- `data/BrewGenius_Product_Guide.md` - The product knowledge base

**That's it.** You decide everything else: chunking, embeddings, vector store, LLM, prompts.

---

## Requirements

### Your Pipeline Must:

1. **Ingest** the product guide and prepare it for retrieval
2. **Retrieve** relevant chunks based on user queries
3. **Generate** accurate, grounded answers using an LLM

### Query Types to Handle:

| Type | Example | Challenge |
|------|---------|-----------|
| Specifications | "What is the water tank capacity of ProBarista Elite?" | Direct lookup |
| Comparisons | "Compare ProBarista Elite vs Studio" | Multi-item synthesis |
| Recommendations | "Which machine is best for a small apartment?" | Understanding user needs |
| Troubleshooting | "My espresso is bitter, what should I do?" | Problem-solution matching |
| Pricing | "What's the cheapest espresso machine?" | Filtering + sorting |
| Calculations | "If I make 4 lattes/day, how long does the water tank last?" | Reasoning + math |
| Edge Cases | "What's the Bluetooth range?" | Handling missing info gracefully |

---

## What to Submit

### 1. Source Code
- Complete, runnable pipeline
- **Must work on first try** - test it yourself before submitting
- Clear entry point (how to run it)

### 2. Architecture Document (1-2 pages)

Explain your choices with **specific justification**:

| Decision | What We Want to See |
|----------|---------------------|
| Chunking strategy | WHY you chose your chunk size, not just "512 is standard" |
| Embedding model | Trade-offs you considered, why THIS model for THIS task |
| Vector store | Why it fits this use case (~100 chunks, single document) |
| Retrieval approach | How you chose k, how you handle low-confidence results |
| Prompt design | How you prevent hallucination, handle different query types |

**Generic explanations will score poorly.** Reference the BrewGenius document specifically.

### 3. Performance Report

Include actual measured data:
- Average response latency (measured, not estimated)
- Average tokens per query (measured)
- Test results on at least 5 different query types

---

## Evaluation Criteria

| Category | Weight | What We're Looking For |
|----------|--------|------------------------|
| Query Accuracy | 40% | Correct answers on standard AND edge-case queries |
| Architecture Design | 25% | Justified decisions, not generic explanations |
| Implementation Quality | 20% | Code quality, error handling, documentation |
| Optimization | 15% | Working optimizations with measured impact |

### We Will Test:

1. **Standard queries** - Can it answer basic product questions?
2. **Adversarial queries** - Does your pipeline:
   - Admit when it doesn't have information?
   - Avoid hallucinating details not in the document?
   - Handle edge cases gracefully?
   - Reason through calculations?
   - Recognize impossible requests?

3. **Code verification** - We will:
   - Run your code following your README
   - Test edge cases (empty query, invalid input)
   - Verify claimed optimizations actually exist
   - Check that documentation matches implementation

### Red Flags That Lower Scores:

- Pipeline never says "I don't know" (hallucination risk)
- Documentation describes features not in code
- Generic explanations that could apply to any RAG project
- Inconsistent coding styles (suggests copy-paste)
- Over-engineered for the task (~100 chunks, not production scale)
- Claims "tested X" but no evidence provided
- Code doesn't run following your instructions

---

## Constraints

- **LLM:** Your choice (OpenAI, Anthropic, local models, etc.)
- **Language:** Any (Python recommended)
- **Libraries:** Any (LangChain, LlamaIndex, custom, etc.)
- **Time:** 90 minutes

---

## Submission Format

Create a ZIP file containing:
```
YourName_RAG/
├── README.md              # Setup + usage instructions (must be accurate!)
├── requirements.txt       # Dependencies with versions
├── src/                   # Your source code
├── architecture.md        # Architecture document with understanding questions
├── performance.md         # Performance report with real measured data
└── data/
    └── BrewGenius_Product_Guide.md
```

**Name your ZIP file:** `YourName_RAG.zip` (e.g., `John_Doe_RAG.zip`)

---

## Tips for Success

### Do:
- **Start simple** - Get basic RAG working first, then optimize
- **Measure everything** - Real numbers, not estimates
- **Document your reasoning** - WHY you made each choice
- **Test edge cases** - Empty queries, nonsense input, missing info questions
- **Be honest about limitations** - "This doesn't handle X well because..."

### Don't:
- **Over-engineer** - This is ~100 chunks, not a production system
- **Copy generic tutorials** - Adapt for BrewGenius specifically
- **Claim what you can't prove** - "I tested X" requires evidence
- **Ignore edge cases** - We will test them
- **Let your pipeline hallucinate** - Better to say "I don't know"

---

## What Makes a Great Submission

1. **Runs perfectly on first try** following your README
2. **Architecture choices are justified** with specific reasoning for THIS task
3. **Handles edge cases** gracefully (admits uncertainty, doesn't hallucinate)
4. **Code is clean and consistent** (not patchwork from multiple sources)
5. **Documentation is accurate** and matches the actual implementation
6. **Performance is measured** with real data, not estimates
7. **Shows understanding** - can explain WHY, not just WHAT

---

**Good luck!** Show us that you understand RAG, not just that you can prompt an AI to generate code.
