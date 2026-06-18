# Pipeline Stages

The Urban AI Scientist pipeline runs three sequential stages.  
Each stage must complete before the next begins.

---

## Stage 1 — Idea Generation

**Duration:** ~5 minutes  
**Skill:** `/idea-creator-zgca`

The system searches for related academic papers (CAMP mode) or directly brainstorms (SEMM mode), then generates a structured research idea including:

- Core problem and motivation
- Proposed method sketch
- Novelty check against existing literature
- Estimated contribution level

**Output file:** `<topic>_idea.md`

---

## Stage 2 — Paper Plan

**Duration:** ~10 minutes  
**Skills:** `/paper-plan-zgca-v2`

Based on the idea from Stage 1, the system generates:

- A full paper outline (Nature-style, claim-first structure)
- A detailed experiment plan with dataset recommendations and baselines
- A figure blueprint (what each figure should show)
- A task queue for the writing stage

**Output files:**
- `PAPER_PLAN.md` — narrative paper plan
- `EXPERIMENT_PLAN.md` — reproducible experiment steps
- `DOWNLOAD_REPORT.md` — datasets found and retrieved for the experiments
- `NATURE_PAPER_PLAN.md` — structured plan used by the writer

---

## Stage 3 — Paper Writing

**Duration:** ~20–40 minutes  
**Skill:** `/paper-writer-zgca`

The system writes the full paper in LaTeX and compiles it to PDF:

- Implements lightweight experiment code
- Generates result tables and figures
- Writes all sections (abstract through conclusion)
- Compiles with `pdflatex` and fixes any LaTeX errors automatically

**Output file:** `main.pdf` (~8–12 pages)

---

## Stage Transitions

The web interface shows a three-step progress indicator:

```
[ Idea ] → [ Plan ] → [ Paper ]
```

Each step lights up when the stage starts and is marked complete when the download button appears.  
You can download a stage's output immediately without waiting for later stages to finish.

---

## Failure Handling

- If any stage fails, the pipeline stops and an error message is shown in the log
- Partial results from completed stages are still downloadable
- Re-submitting the same topic starts a fresh run from Stage 1
