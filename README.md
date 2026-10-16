# Dense LLM System Prompt

A high-density system prompt (<1,500 characters) engineered for **autonomous sysadmin workflows and terminal troubleshooting**[cite: 2]. It eliminates conversational filler, resolves root causes without breaking existing configurations, and prioritizes direct action over delegation[cite: 2].

Optimized for **Google Gemini** (via *Personal context* / *Instructions*) to mitigate verbosity, sycophancy, hallucinated facts, and repetitive retry loops[cite: 2]. Fully compatible with cloud providers (ChatGPT, Claude) and local runtimes (Ollama, LM Studio, llama.cpp)[cite: 2].

---

## Key Capabilities

### 1. Operational Autonomy
* **Tool-first inspection:** Proactively gathers facts using integrated tools instead of asking the user to run checks[cite: 2].
* **Zero-tool fallback:** Provides a single, minimal **read-only** command block to inspect system state when tools are unavailable[cite: 2].
* **Environment awareness:** Detects host OS and active shell automatically[cite: 2].
* **Targeted questioning:** Prompts the user only when required details cannot be inspected programmatically; otherwise, proceeds with stated assumptions[cite: 2].
* **Context preservation:** Resolves follow-ups in order while cleanly queuing new issues[cite: 2].

### 2. Surgical Remediation
* **Root-cause focus:** Delivers permanent, robust fixes rather than superficial patches[cite: 2].
* **Setup preservation:** Inspects dependent chains, applies the minimum necessary edits, and preserves existing formatting and conventions[cite: 2].
* **Controlled scope:** Refactors or redesigns only when explicitly requested[cite: 2].

### 3. Factual Reliability & Rigor
* **Source-backed assertions:** Confirms volatile data (versions, pricing, docs, dates) using primary sources, marking conflicts clearly[cite: 2].
* **Anti-sycophancy:** Rechecks findings upon user pushback but yields exclusively to empirical evidence[cite: 2].
* **Visual parsing:** Extracts legible content from terminal/error images, requesting raw text if readability is compromised[cite: 2].

### 4. Safety Guardrails
* **Ephemeral backups:** Backs up critical targets prior to execution and removes backup copies immediately after verification[cite: 2].
* **Destructive safety:** Executes non-destructive or replacement tasks automatically, requiring explicit confirmation only for unrelated destructive operations[cite: 2].

### 5. Deterministic Output Format
* **Direct commands:** Outputs exactly one explanatory sentence (outlining task and operational risk) followed by a single copy-pasteable, non-interactive command block[cite: 2].
* **File replacements:** Emits complete file contents with explicit path definitions for multi-line configurations[cite: 2].
* **Option ranking:** Highlights the recommended solution and its justification first; summarizes remaining alternatives on a single line[cite: 2].
* **Noise-free syntax:** Strips intros, conversational closings, and em dashes[cite: 2]. Renders math strictly in LaTeX[cite: 2].

### 6. Failure Recovery
* **Loop breaker:** Halts repetitive loops by retrying an alternative strategy exactly once before escalating the blocker[cite: 2].
* **Verified resolution:** Tasks are considered complete only after execution outputs validate the fix[cite: 2].

---

## Installation & Usage

1. Copy the raw prompt from the latest **[Releases]**[cite: 2].
2. **Google Gemini:** Navigate to **Settings → Personal context** (*Instructions for Gemini*) and paste the prompt[cite: 2].
3. **Other Models:** Apply as the system prompt (local engines like Ollama/llama.cpp) or within custom instruction fields (ChatGPT, Claude)[cite: 2].

> *Note: While the prompt is written in English to ensure optimal instruction adherence, the assistant naturally responds in your input language[cite: 2].*
