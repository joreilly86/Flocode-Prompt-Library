# AI Context: Engineering Project

**Purpose:** This file provides project context to AI assistants (Claude, ChatGPT, Gemini, Qwen, etc.) for accurate, relevant engineering assistance. Copy this template into your project root and update each section as your project evolves.

**Best For:** Any AI-assisted engineering project using Python. Place this file where your AI tool reads project context (e.g., `CLAUDE.md`, `.cursorrules`, `ai-context.md`, or paste it into the conversation).

---

## 1. Project Overview

**Project Goal:** [One-sentence description of the project objective]

**Engineering Discipline:** [Structural, Civil, Mechanical, Geotechnical, Electrical, Water Resources, etc.]

**Project Phase:** [Preliminary Design, Detailed Design, Analysis, Review, etc.]

---

## 2. Technical Environment

**Language:** Python

**Environment:** Jupyter Notebook / VS Code

**Package Manager:** uv

**Core Libraries:**
- `pandas` — data manipulation and analysis
- `numpy` — numerical operations and calculations
- `matplotlib`, `seaborn` — static plotting
- `plotly` — interactive visualizations
- `scipy` — scientific and technical computing

**Additional Libraries (add as needed):**
- `polars` — high-performance DataFrames for large datasets
- `pint` — unit handling and conversion
- `sympy` — symbolic mathematics
- `shapely`, `geopandas` — geospatial analysis

## 3. Directory Structure

```
project/
├── data/           # Raw data, datasheets, specifications
├── notebooks/      # Jupyter notebooks for analysis
├── src/            # Reusable Python modules and functions
├── reports/        # Generated reports, figures, summaries
├── calcs/          # Detailed calculation sheets
├── docs/           # Standards, references, project documentation
└── ai-context.md   # This file
```

**Workflow:**
1. Store raw data and specs in `data/`
2. Perform exploratory analysis in notebooks
3. Extract reusable functions to `src/` modules
4. Generate final deliverables in `reports/`

---

## 4. Design Parameters & Constraints

**Key Parameters:**
- [Parameter 1: value, units, source/standard]
- [Parameter 2: value, units, source/standard]

**Critical Constraints:**
- [Constraint 1: description]
- [Constraint 2: description]

**Applicable Codes & Standards:**
- [e.g., ACI 318-19, ASCE 7-22, AISC 360-22, AWWA M11, etc.]

**Load Cases & Combinations:**
- [If applicable: Dead, Live, Wind, Seismic, etc.]

**Material Properties:**
- [e.g., f'c = 4000 psi, fy = 60 ksi, etc.]

---

## 5. Domain-Specific Context

**Background:**
[Brief technical context: What problem are you solving? What analysis methods are you using?]

**Key Equations/Methods:**
[List critical formulas, design methodologies, or calculation procedures]

**Assumptions:**
- [Assumption 1]
- [Assumption 2]

**References:**
- [Paper/textbook citations, design manuals, datasheets]

---

## 6. Coding Conventions

- **Clarity:** Use descriptive variable names with units (e.g., `moment_capacity_kip_ft`, `flow_rate_m3_s`)
- **Docstrings:** All functions must document purpose, arguments, returns, and units
- **Type Hints:** Use Python type hints for function signatures
- **Units:** Explicitly state units in comments, variable names, or DataFrame columns
- **Structure:** Organize notebooks with Markdown headings for report-like readability
- **Validation:** Include sanity checks for engineering-critical calculations (bounds checking, unit consistency)

---

## 7. Current Status

**Completed:**
- [Task 1]
- [Task 2]

**In Progress:**
- [Task 3]

**Outstanding Items:**
- [Task 4 — priority/notes]

**Next Steps:**
- [Immediate next action]

---

## 8. Instructions for AI Assistants

When providing assistance:
- Follow the applicable codes and standards listed above
- Maintain the established coding conventions
- Use the specified units system consistently
- Reference the design parameters and constraints
- Generate code that integrates with the existing directory structure
- Provide engineering rationale for design decisions
- Show step-by-step reasoning for calculations before stating results
- When uncertain about a value, standard, or approach, say so explicitly

**Example queries this context enables:**
- "Using ACI 318-19, write a function to calculate beam shear capacity"
- "Generate a bearing pressure vs. footing width plot using the parameters above"
- "Refactor the moment calculation from the notebook into `src/structural_calcs.py`"
