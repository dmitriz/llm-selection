# PROJECT BACKLOG — llm-selection

This file serves as the **complete strategic record** for the `llm-selection` project.  
It contains all relevant ideas, insights, plans, and instructions discussed — **nothing omitted**.

## 📋 Table of Contents

- [Project Purpose](#-project-purpose)
- [Key Goals](#-key-goals)
- [Core Components](#-core-components)
  - [Model Capability Tracker](#1-model-capability-tracker)
  - [Routing Logic](#2-routing-logic)
  - [Reviewer Agent](#3-reviewer-agent)
  - [Prompt Adaptation Patterns](#4-prompt-adaptation-patterns)
  - [Evaluation Workflows](#5-evaluation-workflows)
  - [Task Classifier](#6-task-classifier-future)
- [Roles & Agents](#-roles--agents)
- [Key Insights & Strategy Notes](#-key-insights--strategy-notes)
- [Experiments](#-experiments)
- [Tasks (Open)](#-tasks-open)
- [Notes](#-notes)

---

## ✅ Project Purpose

Design and maintain a system for **selecting, routing, and evaluating large language models (LLMs)** based on task type, reasoning ability, access methods, costs, reliability, and user-defined preferences.

---

## 🔹 Key Goals

### Catalog & Capabilities

- Create a structured **catalog of available LLMs** (hosted + local)
- Track model capabilities: reasoning, generation, summarization, speed, latency
- Track access methods: OpenAI, Claude, Gemini, Grok, local APIs, etc.

### Routing & Logic

- Develop a model selection and routing logic (manual + automated)
- Enable task-based model decision-making using clear rules
- Document prompt adaptation needs for different models

### Evaluation & Feedback

- Design **reviewer prompts** to evaluate model output reliability and completeness
- Implement multi-model feedback loops: compare answers, escalate, route to reviewer
- Prepare for eventual automation and integration into assistant/agent systems

---

---

## 🔹 Core Components

### 1. Model Capability Tracker

*See detailed design in [models.md](models.md)*

- Name, provider, access type (API/local), rate limits, cost structure
- Token/window limits, search capability, file input support
- Update history, reliability patterns, reasoning depth classification

### 2. Routing Logic

*See detailed design in [routing-strategy.md](routing-strategy.md)*

- Task-to-model mapping table or logic flow
- Conditional decision-making (e.g., if search needed, use X; if local, use Y)
- Model fallback based on latency, token limits, or quota status

### 3. Reviewer Agent

*See detailed design in [reviewer-prompts.md](reviewer-prompts.md)*

- Prompt templates for reviewing output quality, coherence, hallucination risk
- Scoring guidelines and structured review format
- Cross-model comparison prompts

### 4. Prompt Adaptation Patterns

*See detailed implementation in [prompt-patterns.md](prompt-patterns.md) (planned)*

- Variants needed for models that require different formatting (e.g., Claude XML tags)
- Self-evaluation trigger prompts ("explain how you understood this before answering")
- Structure tags or reusable prompt components

### 5. Evaluation Workflows

*See detailed workflows in [evaluation-flows.md](evaluation-flows.md) (planned)*

- Run same prompt across multiple models
- Capture outputs + reviewer evaluation
- Score responses on reasoning, hallucination risk, formatting, insight quality

### 6. Task Classifier (Future)

*See design plans in [task-classifier.md](task-classifier.md) (planned)*

- Classify user requests into task types: research, summarization, validation, generation
- Use classification to trigger routing decisions

---

---

## 🔹 Roles & Agents

- **User/Initiator**: Provides task intent and constraints
- **Router**: Maps task to appropriate model(s)
- **LLM Worker**: Generates or retrieves answer
- **Reviewer**: Evaluates and flags weak or incorrect outputs
- **Decision Layer**: Chooses whether to escalate, switch models, or finalize

---

## 🧠 Key Insights & Strategy Notes

- **Model selection is not static**: capabilities evolve rapidly, so selection logic must be easily editable
- Reasoning models (GPT-4o, Claude Opus) often required for synthesis, logic, ambiguity
- Generation-first models (e.g. Gemini Pro) may be better for formatting, templating, speed
- Reviewers are essential: many LLMs produce superficially plausible, but flawed answers
- Model hallucination is often subtle; detecting it must be part of the process
- **Two-way flow with agents like Copilot** is critical (e.g., Copilot asks LLM → LLM generates solution → Copilot verifies and executes)
- **File- and folder-based context** is more scalable than prompt text alone
- Local quantized models (e.g., via Ollama, llama.cpp) are viable but must be benchmarked
- Cost/rate limits can be offset by chaining: cheap model for draft, powerful model for polish
- **Grok’s search access** is uniquely valuable for community data (X/Twitter)
- **Selection rules should be declarative**, not procedural, for reuse and automation

---

## 🧪 Experiments

- [ ] Run identical prompts across GPT-4o, Claude, Gemini, Perplexity
- [ ] Use reviewer prompt to evaluate each output
- [ ] Compare same prompt with search ON/OFF in GPT-4o and Grok
- [ ] Benchmark latency + quality for local vs API models
- [ ] Test effectiveness of prompt explain-understanding-first strategy
- [ ] Run prompts through a scoring reviewer and compare with human rating
- [ ] Record false-positive hallucination cases and model failure patterns

---

## 🛠 Tasks (Open)

- [ ] Create `models.md` catalog of models, metadata, rate limits, access
- [ ] Create `routing-strategy.md` logic flow or ruleset
- [ ] Design initial reviewer prompt in `reviewer-prompts.md`
- [ ] Prepare a task classifier template or table
- [ ] Define fallback rules based on quota, cost, response failure
- [ ] Add local model testing section (llama.cpp, Mistral, Ollama)
- [ ] Integrate results from Grok search when collecting model performance signals

---

## 📌 Notes

- This backlog grows **continuously**
- All new ideas must be logged here, even if later moved to GitHub Issues
- Do **not** trim or remove ideas unless explicitly archived elsewhere
- This is the **single source of truth** for everything related to LLM selection strategy

---

> End of file.
