# CLAUDE.md — Are-Self Research

Academic papers for the Are-Self project. LaTeX, APA 7th edition (`apa7` document class).

## Papers

All 6 papers have substantial LaTeX outlines in `papers/*/paper.tex`.
Template at `papers/are-self-paper.tex`.

| Paper | Directory | Status | Notes |
|-------|-----------|--------|-------|
| Neuro-Mimetic Architecture | `neuro-mimetic-architecture/` | Most complete draft | Flagship paper. Full sections, but Evaluation has TODOs |
| The Focus Economy | `focus-economy/` | Detailed outline | Has formal math (budget equations, equilibrium analysis) |
| Hippocampus Hypergraph Migration | `hippocampus-hypergraphs/` | Detailed outline | Co-authored with Samuel Frerichs (U. Pittsburgh) |
| LLM Testing Harness | `llm-testing-harness/` | Outline | 5 evaluation dimensions defined |
| CI/CD Sovereignty | `ci-cd-sovereignty/` | Outline | Pipeline-as-pathway mapping |
| Multiplayer Unreal + Autonomous AI | `multiplayer-unreal-autonomous-ai/` | Outline | Case study format |

## Compiling

```bash
cd papers/neuro-mimetic-architecture
pdflatex paper.tex
biber paper          # for bibliography (if .bib exists)
pdflatex paper.tex
pdflatex paper.tex
```

Requires: TeX Live or similar with `apa7` class (`tlmgr install apa7`).
Alternative: import paper directory into [Overleaf](https://overleaf.com).

In the Cowork sandbox, `pdflatex` is at `/usr/bin/pdflatex`. The `apa7` class may need
installation — check with `kpsewhich apa7.cls`.

## Key Technical Details

These inform the paper content:

- **Tick cycle:** PNS → Temporal Lobe → CNS → Frontal Lobe → Parietal/Hippocampus/Hypothalamus
- **Focus Economy:** F₀ = 10 + 0.5(L-1), novelty reward r = α(1-s) if s < 0.90
- **Memory:** pgvector 768-dim embeddings, 90% cosine similarity dedup threshold
- **Addon pipeline phases:** IDENTIFY → CONTEXT → HISTORY → TERMINAL
- **River of Six:** sliding window history with age-based decay
- **CNS node types:** Gate (PK5), Retry (PK6), Delay (PK7), Frontal Lobe (PK8), Debug (PK9)

## Relationship to Docs Site

`are-self-docs/docs/research.md` has summaries of all 6 papers and links to this repo.
The docs site navbar, footer, and homepage feature cards all cross-link to the research page.

## License

Papers: CC BY 4.0. Code examples within papers: MIT.
