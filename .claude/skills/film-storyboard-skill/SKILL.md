---
name: film-storyboard-skill
description: Use when creating storyboards from scripts, generating visual prompts for beat boards or sequence boards, or converting narrative beats into AI-generated images across platforms (Nano Banner, Midjourney, Gemini)
version: 1.0.0
allowed-tools: Read, Write
user-invocable: false
---

# Film Storyboard Skill

Provides the Storyboard Artist with professional film storyboarding methodology and prompt generation capabilities.

## Overview

This skill helps convert scripts into visual storyboards, supporting the complete three-stage process:

1. **Beat Breakdown** - Identify 9 key narrative moments from the script
2. **Beat Board (9-Grid)** - Generate a visual prompt for each beat
3. **Sequence Board (4-Panel)** - Expand a key beat into a continuous shot sequence

## Core Principles: 4C Framework

1. **Clear** - Every prompt is unambiguous
2. **Concise** - Detailed but not bloated (Visual Description: 80-120 words, Lighting & Mood: 30-50 words)
3. **Consistent** - Character/scene/lighting and color stay consistent across all prompts
4. **Progressive** - Refine layer by layer from the 9-grid to the 4-panel sequence

## Quick Start

### Generate a Beat Breakdown

```markdown
Identify 9 key narrative moments from the script, including:

- Beat number and title
- Timestamp/page number
- Core action
- Emotional value
  Use template: templates/beat-breakdown-template.md
```

### Generate a Beat Board

For Nano Banner (recommended):

```markdown
EPISODE {XX}: BEAT BOARD VISUAL SCRIPT

Beat 1: [Title]
Visual Description: [80-120 word visual description]
Lighting & Mood: [30-50 words on lighting and atmosphere]
```

For Midjourney:

```
One independent prompt per beat + --ar 16:9 --style cinematic --v 6
```

### Generate a Sequence Board

Select a key beat and expand it into 4 continuous shots, maintaining:

- The 180-degree rule
- Character appearance consistency
- Lighting continuity

## Key Constraints

**Strictly prohibited**:

- ❌ Frontmatter metadata in output files
- ❌ Template instructions or notes
- ❌ "Next step" directives

**Must include**:

- ✅ Canonical character description
- ✅ Key identifiers repeated verbatim
- ✅ The appropriate platform format (Nano Banner/Midjourney/Gemini)

## Detailed Resources

### Methodology Guide 📖

- [storyboard-methodology-playbook.md](storyboard-methodology-playbook.md) - Complete storyboard methodology
  - The four pillars in detail
  - Beat selection criteria
  - Shot composition and cinematography
  - Continuity management
  - Advanced film techniques (montage, transitions, time and space manipulation)

### Prompt Writing 📖

- [gemini-image-prompt-guide.md](gemini-image-prompt-guide.md) - Prompt optimization guide
  - Narrative descriptive style
  - Character consistency techniques
  - Lighting description methods
  - Nano Banner format optimization

### Platform and Style Reference 📖

- [REFERENCE.md](REFERENCE.md) - Platform features and style library
  - Nano Banner vs Midjourney vs Gemini format comparison
  - Library of 7 visual styles (photorealistic, anime, concept art, etc.)
  - 6 candidate lighting schemes
  - Aspect ratio options

### Templates

- [templates/beat-breakdown-template.md](templates/beat-breakdown-template.md)
- [templates/beat-board-template.md](templates/beat-board-template.md)
- [templates/sequence-board-template.md](templates/sequence-board-template.md)

## When to Use

**Automatic trigger scenarios**:

- User requests "generate beat breakdown"
- User requests "create beat board" or "9-grid"
- User requests "generate sequence board" or "4-panel sequence"
- Director feedback requires visual consistency revisions

**Manual reference scenarios**:

- Unsure about prompt format
- Choosing a visual style
- Resolving character consistency issues
- Optimizing platform-specific formats

## Quick Platform Selection

- **Prioritizing consistency** → Nano Banner (generates the full 3x3 grid in one pass)
- **Need fine-grained control** → Midjourney v6
- **Rapid prototyping** → Gemini Imagen 3

---

**Usage**: The Storyboard Artist agent references this skill automatically. The methodology and guides (marked 📖) use progressive disclosure and are consulted only when needed.
