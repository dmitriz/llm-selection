# PROJECT BACKLOG — llm-selection

This project aims to support strategic model selection for LLM tasks. It will track model capabilities, reasoning depth, rate limits, file support, access type (API/local), and usage strategies.

---

## ✅ Core Goals

- Catalog available models (GPT-4o, Claude, Gemini, Perplexity, local models)
- Track API access methods, rate limits, pricing, latency, reliability
- Differentiate models by reasoning strength vs generation speed
- Record model-specific prompt adaptation patterns
- Design a lightweight routing logic for task-type-to-model mapping
- Enable reviewer prompts to assess model output reliability
- Plan for multi-model evaluation loops (e.g., Grok + Claude + GPT-4o)
- Begin evaluation logging for performance and failures

---

## 🧠 Key Ideas to Track

- Reasoning models vs generative models: how to choose
- Structured vs unstructured prompt input
- Task classification: research, summarization, synthesis, validation
- Local quantized model usage and constraints (e.g., llama.cpp, Ollama)
- Router design: file-based input → task → model(s) → reviewer loop
- Use of assistant-agent separation (router, reviewer, executor)
- Explore how to collect model performance data over time
- Evaluate when to use search vs static LLM
- Decision trees, scorecards, or rule-sets for model choice

---

## 🧪 Suggested Experiments

- Run identical prompts across GPT-4o, Claude Opus, Gemini Pro
- Use reviewer prompt to evaluate each output
- Compare search-enabled vs search-disabled runs
- Benchmark against latency, reasoning quality, hallucination frequency

---

## 📥 Tasks (Initial)

- [ ] Create `models.md` for cataloging available LLMs
- [ ] Add `routing-strategy.md` to outline logic by task type
- [ ] Prepare reviewer prompt set in `reviewer-prompts.md`
- [ ] Design and test a selection prompt (e.g., “Which model should I use for X?”)

---

> You can move any of these items into GitHub Issues or Projects if needed. This backlog will grow as other repos are integrated.
