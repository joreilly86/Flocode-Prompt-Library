# Compact and Continue

**Purpose:** Condense a lengthy technical conversation into a focused handoff document. Use this when approaching context limits or when you need to start a fresh session while preserving all critical information.

**Best For:** Long AI sessions nearing context limits, team handoffs, or resuming work after a break.

## The Prompt

```
Generate a technical handoff summary with the following sections:

1. Objective and scope
2. Current status and key decisions made
3. Critical design parameters, constraints, and assumptions
4. Outstanding items requiring resolution (with priority)
5. Next steps — the specific next action to take when resuming

Omit iterative discussion, abandoned approaches, and troubleshooting history. Focus on actionable information only.

Provide complete context so a peer professional (or a new AI session) can continue immediately without re-reading the full conversation.
```

## Usage Notes

- Paste this prompt into your current session when the conversation is getting long or the AI starts losing earlier context
- Copy the generated summary, open a new session, and paste it as your opening message
- Works across all AI tools — not specific to any single assistant
- For engineering projects, the summary should preserve: applicable codes, load cases, material properties, and design decisions
- Combine with [coding-context.md](../engineering/coding-context.md) for a complete project handoff

## Example Usage

**Input**: After a long session designing a reinforced concrete retaining wall — calculations, code checks, design iterations, and several abandoned approaches

**Output**:
```
## Objective
Design cantilever retaining wall for 3.5m retained height, granular backfill.

## Status
Stem and base proportions finalized. Sliding and overturning checks pass.
Key decision: selected 400mm stem thickness based on ACI 318-19 crack control.

## Parameters
- Retained height: 3.5m, level backfill
- Soil: φ=32°, γ=18.5 kN/m³, Ka=0.307
- Concrete: f'c=30 MPa, fy=500 MPa
- Bearing capacity: 200 kPa (from geotech report dated 2024-11-15)

## Outstanding
1. [High] Stem reinforcement design — flexural steel not yet sized
2. [Medium] Drainage detail behind wall — weephole spacing TBD

## Next Steps
Size vertical reinforcement in stem for factored bending moment of 145 kN·m/m.
```
