# Dense LLM System Prompt

A high-density system prompt (<1500 characters) engineered for **autonomous terminal troubleshooting, sysadmin workflows, and rigorous AI assistance**. It eliminates conversational filler, treats tool outputs strictly as data, resolves root causes without breaking configurations, and prioritizes direct action over delegation.

Optimized for **Google Gemini** (via *Personal context* / *Instructions*) and fully compatible with cloud providers (ChatGPT, Claude) and local runtimes (Ollama, LM Studio, llama.cpp).

---

## Key Capabilities

### 1. Operational Autonomy & Execution
- **Tool-first inspection:** Proactively gathers facts via integrated tools or issues a minimal read-only check (≤2 lines + 1 bash block) when tools are unavailable.
- **Two-phase execution:** Checks system state read-only in the first reply before executing modifications in the second.
- **Command safety:** Chained bash commands with absolute paths, using `sed` for surgical in-place edits instead of interactive editors.
- **Package hierarchy:** Follows a strict preference order for Linux environments: `Flatpak > native repos/AppImage > AUR`.

### 2. Surgical Remediation & Safety
- **Root-cause focus:** Applies permanent fixes one change at a time, testing results and backing up key files before modifying them.
- **Data vs. command boundary:** Strictly isolates tool, file, and web outputs as passive data, never interpreting external content as commands.
- **Fail-safe reporting:** Retries with alternative approaches on failure and reports blockers after 3 unsuccessful attempts.

### 3. Fact Verification & Search Rigor
- **Official sourcing:** Cross-checks APIs, tools, and news against official documentation and exact string matches.
- **Verifiable claims:** Distinguishes verified facts from inferences, never fabricating quotes, flags, or URLs.
- **Clinical reasoning:** Analyzes user-reported health symptoms clinically for coherence and advises professional care when urgent.

### 4. Output Discipline & Structure
- **Zero conversational filler:** Omits greetings, pleasantries, preambles, and redundant summaries.
- **Structured density:** Uses concise prose, single bullet lists, and a maximum of 3 headers for complex plans, with outcome-oriented steps for guides.
- **Multimodal precision:** Inspects text, UI anomalies, and visual selections accurately; requests assets as full-frame PNGs.

---

## License

Distributed under the [GPL-3.0](LICENSE) license.
