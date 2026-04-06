# Are-Self Research

Academic papers and technical whitepapers for the [Are-Self](https://github.com/scipraxian/are-self-api) project — an open-source, neuro-mimetic AI reasoning engine that runs on consumer hardware.

## Papers

| Paper | Status | Authors | Description |
|-------|--------|---------|-------------|
| **[Neuro-Mimetic Architecture](papers/neuro-mimetic-architecture/)** | Draft | Michael Clark | The flagship paper. Describes the brain-region software architecture, tick-cycle execution model, addon pipeline, and real-time event system. |
| **[The Focus Economy](papers/focus-economy/)** | Draft | Michael Clark | Bounded autonomy through incentive-aligned resource management. How linking execution budgets to memory novelty prevents degenerate agent behavior. |
| **[Hippocampus Hypergraph Migration](papers/hippocampus-hypergraphs/)** | Draft | Samuel Frerichs, Michael Clark | Proposed migration from flat Engram M2M relations to a hypergraph memory model with typed relationships (causal, temporal, contradicts, etc.). |
| **[LLM Testing Harness](papers/llm-testing-harness/)** | Draft | Michael Clark | Evaluating local models for agent-specific criteria: tool call compliance, multi-turn consistency, focus efficiency, memory formation quality, and quantization effects. |
| **[CI/CD Sovereignty](papers/ci-cd-sovereignty/)** | Draft | Michael Clark | Using Are-Self's neural pathway system as a self-hosted CI/CD orchestrator with AI-assisted failure diagnosis. |
| **[Multiplayer Unreal + Autonomous AI](papers/multiplayer-unreal-autonomous-ai/)** | Draft | Michael Clark | Case study of building a multiplayer Unreal Engine project with Are-Self as build engineer and project manager. |

## Relationship to Code

These papers describe the architecture, theory, and evaluation of the Are-Self system. The code lives in:

- [are-self-api](https://github.com/scipraxian/are-self-api) — Django backend (brain regions as Django apps)
- [are-self-ui](https://github.com/scipraxian/are-self-ui) — React frontend (graph editor, monitor, reasoning view)
- [are-self-docs](https://github.com/scipraxian/are-self-docs) — Documentation site at [are-self.com](https://are-self.com)

## Format

Papers are written in LaTeX using the APA 7th edition format (`apa7` document class). See `templates/are-self-paper.tex` for the base template.

### Compiling

```bash
cd papers/neuro-mimetic-architecture
pdflatex paper.tex
biber paper
pdflatex paper.tex
pdflatex paper.tex
```

Or use [Overleaf](https://overleaf.com) for collaborative editing — import the paper directory and it compiles in the browser.

### Requirements

- A LaTeX distribution (TeX Live, MiKTeX, or MacTeX)
- The `apa7` document class (`tlmgr install apa7`)
- Biber for bibliography processing

## Contributing

These papers are living documents that evolve alongside the codebase. If you're interested in contributing research, see the [Contributing Guide](https://github.com/scipraxian/are-self-docs/blob/main/docs/contributing.md) and open an issue describing your proposed contribution.

## License

Papers are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Code examples within papers are MIT licensed, consistent with the main project.
