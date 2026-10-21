# Evaluation goal

Evaluate timely news for one specific reader: someone who uses AI models and coding agents every day, pays for at least one subscription, and mainly wants to know which model to use, what it costs, and how far it can be pushed.

What this reader cares about, in rough order:

1. Model releases and capability changes — Claude, GPT/Codex, Gemini, GLM, Kimi, DeepSeek, Qwen, Ollama and comparable models.
2. Subscription plans, pricing, quotas, rate limits, throttling and access restrictions — anything that changes what they get for their money.
3. Coding agents and developer tooling — Claude Code, Codex CLI, Cursor, opencode, Kiro, MCP and similar.
4. Access routes — API relays and proxies, regional availability, account bans, key revocation.
5. Open-weight models that can realistically be run or self-hosted.
6. GitHub projects that are newly trending or that ship a meaningful new capability.
7. AI put to work on physical hardware — microcontroller and single-board projects (ESP32, Raspberry Pi and similar), emulation and platform ports that make one device run another platform's software, and any project where a model visibly makes a device do something it could not do before.

What this reader does not care about: server and datacenter operations, container and network plumbing, consumer device reviews and shopping news, general software-engineering practice, academic papers without a usable release, and funding or personnel news unless it changes what a product can do or what it costs.

# Scoring rubric

- **9-10: Changes a decision.** A major model release or capability jump from a leading provider; a subscription plan, price, quota or access change that affects many users; a widely felt ban, throttling or downgrade event; a coding tool gaining or losing a capability that changes which tool people pick.
- **7-8: Worth knowing today.** A meaningful minor version, a single vendor's price or quota adjustment, a useful new tool or open-weight model, hands-on comparison data that would influence a choice, or a concrete workflow, prompt, configuration or runnable project the reader could copy today.
- **5-6: Useful but not urgent.** Routine releases, industry analysis, secondary vendors, incremental tooling improvements.
- **3-4: Low priority.** Infrastructure and operations, engineering practice unrelated to model choice, research without a usable artifact, policy news with no practical effect on access.
- **0-2: Noise.** Spam, promotion, off-topic material, trivial updates, and headlines that promise more than the source delivers.

# Evaluation guidance

Weight concrete, checkable change over commentary: a stated price, quota, version number, availability change or benchmark result outranks an opinion piece about the same event. Reports of throttling, silent downgrades, bans or quota cuts are substantive when they carry reproducible evidence, and should not be dismissed as complaints.

Judge relevance to this reader before judging general importance. A technically impressive infrastructure or systems story that changes nothing about which model to use or what it costs belongs at 3-4, not 8.

How much the reader can act on something outranks how many people it affects. A post that shows a working workflow, prompt, configuration or installable project the reader could copy today belongs at 7-8 even if it reached only one person. A major vendor announcement with nothing the reader can do differently — funding, personnel, stock moves, policy with no impact on access, benchmark claims without reproducible detail — caps at 5 however widely it is discussed.

Hardware and emulation stories are scored on whether the artifact runs. A published project with source code, a parts list or install steps, and evidence that it works scores 7-8 even when the subject is not an AI model. A demo video with no code, a vendor concept render, or a port that only runs on hardware almost nobody owns scores 3-4.

Do not reward hype, do not treat popularity as importance, and do not raise a score because a subject is broadly discussed.

Use three to five specific topic tags.
