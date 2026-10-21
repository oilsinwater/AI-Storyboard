---
name: scriptwriter-skill
description: Use when creating episodic scripts, ensuring series continuity, adapting story concepts into visual narratives, or preparing scripts with sufficient beats for storyboarding
version: 1.0.0
allowed-tools: Read, Write, Bash(ls:*)
user-invocable: false
---

# Scriptwriter Skill

Provides the Scriptwriter with the expertise to create high-quality, structured scripts, supporting series continuity and sequel creation based on previous episodes.

## Overview

This skill supports creating:

- **Structurally complete scripts** - Three-act structure with 9+ key narrative moments placed at the structural anchors (Hook, Inciting Event, First Plot Point, First Attempt, Pinch Point, Midpoint, Third Plot Point, Climax, Resolution)
- **Continuing series episodes** - Maintaining character, setting, and style consistency
- **Visual scenes** - Detailed descriptions that are easy to convert into storyboards

## Core Principles

### 1. Visual First

The script must be easy to convert into storyboards. Avoid abstract psychological description; use concrete visual description.

❌ **Abstract**: Emma feels confused and afraid.
✅ **Visual**: Emma's eyes widen, her fingers trembling as she turns the pages. A bead of sweat slides down her forehead.

### 2. Character Consistency

- Establish a canonical appearance description (first appearance)
- Keep key identifiers consistent in later episodes
- Develop personality gradually and plausibly

### 3. Character Spine

Define before writing: the protagonist's **Lie**, **Want** (a visible Outer Goal: Win, Stop, Escape, or Retrieve), **Need**, **Ghost** (prior wound), and **Stakes**. The story ends when the Want converges with the Need. An antagonist with a reason makes every protagonist move backfire.

### 4. Clear Structure

**Three-act structure** with percentage anchors:

- Act One (~25%): Setup / Ask - Hook in the Normal World, Inciting Event (~12%), First Plot Point (20-25%: the choice that sets the goal and poses the dramatic question)
- Act Two (~50%): Confrontation / Acceptance - First Attempt, First Pinch Point (~37%), Midpoint (50%: from reaction to action), Third Plot Point (~75%: the low point, the Act II/III turn)
- Act Three (~25%): Resolution / Answer - Climax (~90%), Resolution (New Normal, last ~2%)

### 5. Sufficient Beats

Ensure the script contains **at least 9** clear, visual turning points, one at each anchor. Every scene must turn: the lead leaves in a different emotional state (mad, glad, sad, scared) than they entered, and the scene passes the Mamet check (who wants what, what if they fail, why now).

## Quick Start

### Process for Creating a New Episode

**Step 1: Review the series history**

```bash
# View existing episodes
ls script/

# Read previous episodes to understand character and plot development
```

**Step 2: Conceive the story from user input**

The user may provide:

- Theme keywords (e.g. "betrayal", "discovering the truth")
- Plot direction (e.g. "Character A discovers a secret")
- Emotional tone (e.g. "suspenseful", "heartwarming")

**Step 3: Plan the structure**

- Carry forward the previous episodes' world and character states
- Write the character spine (Lie, Want, Need, Ghost, Stakes) and a logline: when [inciting event] happens, [protagonist] decides to [action] against [antagonist]
- Decide the story kind (Milieu, Idea, Character, Event) so the ending matches the beginning
- Design 9+ key narrative moments, one per structural anchor
- Arrange the three-act structure

**Step 4: Write the script**

Use the standard scene format, ensuring:

- Scene heading: `## Scene {X} - {INT./EXT.} {Location} - {Time}`
- Characters have a full appearance description on first appearance
- Action is in present tense and visual
- Every scene turns (Goal → Conflict → Disaster, then Reaction → Dilemma → Decision)
- Enough beat candidates (≥9)

**Step 5: Output**

```
File naming: script/ep{XX}-{title}.md
Example: script/ep03-betrayal.md
```

## Series Continuity Checklist

Before creating a new episode:

- [ ] All previous episodes have been read
- [ ] Character appearance descriptions are consistent with previous episodes
- [ ] Character relationship states match the end of the previous episode
- [ ] Unresolved plot threads are considered or advanced
- [ ] World-building has no contradictions
- [ ] Visual style and atmosphere remain consistent

## Output Constraints

**Strictly prohibited**:

- ❌ Frontmatter metadata
- ❌ Template instructions
- ❌ Overly abstract psychological description
- ❌ Scenes lacking visual detail

**Must include**:

- ✅ Scene number, location, time
- ✅ Appearance description for characters on first appearance
- ✅ Visual scenes and action
- ✅ Enough key moments (≥9 beat candidates, one per structural anchor)
- ✅ Complete three-act structure (Hook, Inciting Event, First Plot Point, Pinch, Midpoint, Third Plot Point, Climax, Resolution)

## Detailed Resources

### Writing Guidance 📖

- [GUIDELINES.md](GUIDELINES.md) - Detailed writing guidelines
  - Scene format specification (scene headings, time labels, the scene turn, Scene/Sequel, Mamet check)
  - Character first-appearance rules and body-first design
  - Character spine (Lie, Want, Need, Ghost, Stakes; the 4-Goal Rule)
  - Action description best practices
  - Beat distribution guidance (9 beats at the structural anchors)
  - Three-act structure in detail, MICE, logline
  - World-building rules (Sanderson's laws, transformations)
  - Dialogue writing techniques
  - Output checklist

### Templates

- [templates/episode-template.md](templates/episode-template.md) - Standard episode script format

## When to Use

**Automatic trigger scenarios**:

- User requests "create a new episode"
- User provides a story concept that needs to be turned into a script
- Material needs to be prepared for the Storyboard Artist

**Manual reference scenarios**:

- Unsure about scene format
- Handling series continuity issues
- Planning beat distribution
- Resolving character consistency issues

## Example Scene Format

```markdown
## Scene 5 - INT. Subway Car - Night

The car is dim; white fluorescent lights flicker on and off. A few discarded newspapers lie scattered across the empty seats.

EMMA (25, long silver hair, wearing a dark red coat) sits by the window and opens an old leather-bound notebook.
Dense handwritten symbols and a glowing six-pointed star pattern inside are reflected on her face.

Suddenly, all the lights go out.
```

---

**Usage**: The Scriptwriter agent references this skill automatically. The methodology and guides (marked 📖) use progressive disclosure and are consulted only when needed.
