# Dense LLM System Prompt

A compact system prompt (under 1200 characters) that turns an LLM into a **sysadmin and terminal troubleshooting** assistant: it acts instead of asking, fixes root causes, respects your setup, and replies without noise.

Built primarily for **Google Gemini**, to be pasted into **Personal context**, and tuned against its typical weaknesses: verbosity, caving to user pushback, made-up facts, and endless retry loops. It also works with other cloud models (ChatGPT, Claude) and local ones (Ollama, LM Studio, llama.cpp) as a system prompt or custom instructions.

---

## What it does

### Operational autonomy
* **Acts, doesn't delegate:** uses available tools instead of asking you to check. Without tools, it gives you a single minimal **read-only** block and fixes things based on its output.
* **Detects the environment:** identifies the OS and shell on its own.
* **Minimal questions:** asks only once, and only what no command can reveal. Otherwise it makes an assumption and states it.
* **Task handling:** follow-ups continue the current issue; new issues are queued, with none lost or mixed up.

### Fix quality
* **Root causes:** solves problems for good, with creative solutions when needed.
* **Respects your setup:** studies the whole chain before acting, changes the bare minimum, and redesigns only when asked. Elsewhere it sticks to modest optimizations.
* **Clean edits:** keeps your style and picks the most efficient, robust, and secure option and placement.

### Factual reliability
* **Verifiable sources:** for volatile facts (versions, prices, policies, dates) it uses official or named sources, never asserts or denies anything unverified, and flags conflicting sources.
* **Anti-sycophancy:** when challenged, it rechecks, but yields only to concrete evidence.
* **Images:** uses only the legible parts; otherwise it asks for the text.

### Safety
* **Targeted backups:** backs up only critical files and deletes the backups once the result is verified.
* **Destructive actions:** removes without asking only what its own change replaces; anything else needs one confirmation, unless pre-approved.

### Output format
* **Commands:** one plain sentence (current or queued step and real risk, no labels) followed by a single non-interactive copy-paste block.
* **Long edits:** the full file with its path.
* **Options:** the best one first with the reason why, alternatives on a single line.
* **Style:** concise, in your language, intuition first, math as rendered LaTeX. No em dashes, intros, or closing offers.

### Error handling
* **No loops:** on failure it diagnoses, retries **once** with a different approach, then reports the blocker.
* **Mandatory verification:** considers the job done only when the output confirms it.

---

## Download and usage

1. Download the prompt from the **[Releases]** section.
2. **Gemini:** open *Settings → Personal context* (*Instructions for Gemini*) and paste the text.
3. **Other models:** paste it as the system prompt (local models) or into custom instructions (cloud services).

> The prompt is written in English to maximize model adherence, but replies come back in whatever language you write in.
