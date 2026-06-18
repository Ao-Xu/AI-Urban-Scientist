# Getting Started

## Prerequisites

You need one of the following to use the service:

1. **A passphrase** — contact the maintainer
2. **An Anthropic API Key** — create one at [console.anthropic.com](https://console.anthropic.com)

---

## Quick Start (3 steps)

1. Open **[the website](https://cocoa-heap-turbulent.ngrok-free.dev)**
2. Enter your passphrase (or API key), choose a method, enter your topic
3. Click **Launch** and wait — download buttons appear as each stage completes

---

## Choosing Between CAMP and SEMM

### CAMP — Paper-Retrieval Driven

CAMP first retrieves related academic papers for your topic, then generates research ideas grounded in the existing literature.

**Best for:**
- Topics where existing literature matters
- When you want ideas that are clearly differentiated from prior work
- More rigorous novelty analysis

**Slower** — paper retrieval adds time.

### SEMM — Direct Generation

SEMM generates research ideas directly from the topic description without retrieving papers first.

**Best for:**
- Exploratory ideation
- Topics where you already know the literature
- Faster results

---

## Understanding the Output

### Idea (Stage 1)

A Markdown file containing:
- Problem statement
- Proposed method
- Novelty analysis
- Potential contribution

### Paper Plan (Stage 2)

Markdown files containing:
- Structured paper outline
- Experiment plan with baselines
- Dataset recommendations
- Expected results

### Paper PDF (Stage 3)

A compiled PDF containing:
- Full LaTeX paper (~8–12 pages)
- Abstract, introduction, method, experiments, conclusion
- Figures and tables (auto-generated)

---

## Tips for Good Results

- **Be specific** — "traffic prediction in Beijing using transformer models" yields better results than just "traffic prediction"
- **English topics** tend to produce more coherent papers (the pipeline is tuned for English academic writing)
- **Chinese topics** are supported and will produce Chinese-language content where appropriate
