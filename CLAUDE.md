# CLAUDE.md

## Project Overview

**Flocode Prompt Library** is a collection of recursive, domain-specific AI prompts for professional engineers. The prompts generate other specialized prompts, frameworks, and workflows that scale across engineering domains including mining, power, water resources, infrastructure, and industrial sectors.

This is a **content library** — not a software application. There are no build steps, test suites, or runtime dependencies. The "code" is prompt text in Markdown files designed to be copied into AI assistants (Claude, ChatGPT, Gemini, Qwen, etc.).

## Repository Structure

```
Flocode-Prompt-Library/
├── CLAUDE.md                        # This file — AI assistant guidance
├── README.md                        # Project introduction and quick-start guide
├── .claude/
│   └── settings.local.json          # Claude Code permission settings
├── core-prompts/                    # Recursive prompt generators (start here)
│   ├── prompt-generator.md          # Meta-prompt: creates domain-specific AI assistants
│   ├── context-engineering-framework.md  # Generates project structures and workflows
│   └── compact-and-continue.md      # Context handoff utility for session transitions
├── LICENSE                          # MIT License
└── engineering/                     # Pre-built domain-specific prompts
    ├── engineering-ai-assistant.md   # PE-level comprehensive support with code compliance
    ├── personal-engineering-assistant.md  # Python & hydropower focused assistant
    ├── technical-writing-assistant.md    # Engineering document standards and style
    ├── coding-context.md             # Project context template for AI assistants
    ├── meeting-transcription.md      # Technical meeting minutes generator
    ├── drawing-analysis-assistant.md # Multimodal drawing and image analysis
    ├── calculation-review-assistant.md  # QC review of engineering calculations
    └── specification-writer-assistant.md # CSI MasterFormat specification drafting
```

### Directory Purposes

- **`core-prompts/`** — Recursive generators. These prompts create other prompts. They are the foundation of the library.
- **`engineering/`** — Ready-to-use specialized prompts for common engineering tasks. Each file is self-contained.

## Content Conventions

### Prompt File Format

Every prompt file follows a consistent structure:

1. **Title** — H1 heading with the prompt name
2. **Purpose** — What the prompt does and who it's for
3. **The Prompt** — The actual system prompt text (usually in a blockquote or code block)
4. **Usage notes** — How to use, example queries, or customization guidance

### Writing Style

- **Professional and precise** — no marketing fluff or filler language
- **Engineering-first** — references to applicable codes and standards (ACI, ASCE, AISC, AWWA, IBC, NEC, ASHRAE)
- **Safety-conscious** — always emphasize professional responsibility, verification, and human oversight
- **Concise** — every sentence should add value

### Key Principles Embedded in Prompts

- Professional engineers retain **full responsibility** for validating AI outputs
- Prompts must reference **applicable codes and standards** where relevant
- **Verification protocols** and safety factors should be explicit
- **Recursive design** is preferred — prompts that generate other prompts provide more value than single-function prompts

## Working With This Repository

### Adding a New Prompt

1. Determine if it belongs in `core-prompts/` (generates other prompts) or `engineering/` (standalone specialist)
2. Create a new `.md` file with a clear, descriptive filename using kebab-case (e.g., `geotechnical-analysis-assistant.md`)
3. Follow the existing file format: title, purpose, prompt content, usage notes
4. Update `README.md` to list the new prompt in the appropriate section

### Editing Existing Prompts

- Preserve the existing structure and tone
- Do not add unnecessary verbosity or marketing language
- Ensure any referenced codes/standards are current editions
- Keep prompts self-contained — each file should work independently

### Quality Criteria for Prompts

Prompts in this library should:
- Generate other specialized prompts (recursive value) OR solve real engineering challenges
- Maintain professional standards and code compliance
- Work across multiple projects or domains
- Emphasize safety, verification, and professional judgment

## Git Workflow

- **Main branch:** `main`
- **Feature branches:** `claude/<description>-<id>` pattern
- **Commit messages:** Descriptive, imperative mood (e.g., "Add geotechnical analysis prompt")
- **No CI/CD** — changes are reviewed manually

## Known Issue

The `README.md` references a `specialized/` directory in some links, but the actual directory is named `engineering/`. Keep this in mind when updating documentation or adding new files — use `engineering/` as the canonical directory name.

## Technical Context (From coding-context.md)

When prompts reference a Python engineering workflow, the standard stack is:
- **Language:** Python
- **Package manager:** uv
- **Environment:** Jupyter Notebook / VS Code
- **Core libraries:** pandas, numpy, matplotlib, seaborn, plotly, scipy
- **Naming convention:** Descriptive variables with units (e.g., `moment_capacity_kip_ft`)
- **Requirements:** Docstrings, type hints, explicit units in variable names and comments
