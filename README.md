# AI Storyboard Production System

An AI-driven storyboard artist system built on the Claude Agent + Skill architecture, used to automate the film storyboarding workflow.

## System Overview

This system coordinates a **Producer** with four specialized sub-agents to automatically generate structured storyboard prompts:

```
Producer Agent (CLAUDE.md)
├── Scriptwriter — Generates story scripts
├── Storyboard Artist — Creates beat breakdowns, 9-grid and 4-panel prompts
├── Director — Reviews all outputs for quality control
└── Animator — Generates motion prompts for video generation
```

### Core Value

- **Efficiency**: An automated workflow from concept to prompts, reducing manual work by roughly 80%
- **Consistency**: Strict character/scene/lighting inheritance reduces the randomness of AI generation
- **Professional standards**: Based on film storyboarding methodology, following cinematography and editing principles
- **Quality control**: Automated director review and revision loop
- **Resumable**: Document-driven; after an interruption, work can resume by checking progress
- **Multi-platform**: Supports Nano Banner, Midjourney, Gemini, DALL-E

## Complete Workflow

### The Full 5-Stage Process

```
0. Script Generation (story creation)
   Input: Story concept, genre, theme
   Output: Complete script with scenes, characters, dialogue

1. Beat Breakdown (9 key narrative moments)
   Input: Script + visual style configuration
   Output: 9 key narrative anchors
   Review: Director checks completeness, clarity, selection quality

2. Beat Board (9-grid storyboard)
   Input: Approved beat breakdown
   Output: 9 static image prompts (visual baseline)
   Review: Director checks consistency, coverage, prompt format

3. Sequence Board (4-panel sequence)
   Input: Approved beat board
   Output: Continuous 4-shot sequence prompts (expanding a key moment)
   Review: Director checks motion continuity, axis stability, inheritance rules

4. Motion Prompts (video generation)
   Input: Approved sequence board
   Output: Dynamic motion prompts for video models
   Review: Director checks conciseness, physical feasibility, focus

All prompts are written in English for the best AI compatibility
```

## Project Structure

```
project/
├── script/                              # Script source files (created by the user)
│   ├── ep01-awakening.md
│   └── ep02-revelation.md
│
├── outputs/                             # Generated artifacts (created automatically)
│   ├── beat-breakdown-ep01.md           # Beat breakdown
│   ├── beat-board-prompt-ep01.md        # 9-grid prompts
│   ├── sequence-board-prompt-ep01.md    # 4-panel sequence prompts
│   └── motion-prompt-ep01.md            # Motion prompts
│
└── .claude/                             # System configuration
    ├── agents/                          # Agent definitions
    │   ├── storyboard-artist.md
    │   ├── director.md
    │   ├── animator.md
    │   └── scriptwriter.md
    │
    └── skills/                          # Skill packages
        ├── film-storyboard-skill/       # Storyboard methodology
        ├── storyboard-review-skill/     # Review standards
        ├── animator-skill/              # Motion prompt methodology
        └── scriptwriter-skill/          # Screenplay creation methodology
```

## Installation

There are two ways to make the agents and skills available to Claude Code.

**Option A: Work inside this repository**

Clone the repo and start Claude Code in it. The agents in `.claude/agents/` and the skills in `.claude/skills/` are loaded automatically as project-level components, and `.claude/CLAUDE.md` configures Claude as the Producer.

**Option B: Install as a plugin in another project**

```
/plugin install ai-storyboard --marketplace oilsinwater/AI-Storyboard
```

On Claude Code versions before 2.1.275, add the marketplace first:

```
/plugin marketplace add oilsinwater/AI-Storyboard
/plugin install ai-storyboard@ai-storyboard
```

The plugin ships the four sub-agents and their skills. It does not ship the Producer instructions, so copy the contents of `.claude/CLAUDE.md` into the consuming project's own `CLAUDE.md`.

## Quick Start

### 1. Create a Script

Create a new episode script in the `script/` directory:

```markdown
# Episode 01: Awakening

> **Series Continuity Note**: First episode of the series, introducing the protagonist and the world.

## Scene 1 - INT. Emma's Apartment - Early Morning

A tiny studio apartment, sunlight spilling in through grimy windows...

EMMA (25, waist-length straight silver hair, pale skin, violet eyes,
wearing a long black trench coat and a white turtleneck) sits on the edge of the bed...
```

### 2. Generate a Beat Breakdown

Interact with Claude:

```
Please generate a beat breakdown for ep01
```

The system will automatically:

1. Scriptwriter reads `script/ep01-awakening.md`
2. Storyboard Artist identifies 9 key narrative moments
3. Director reviews quality
4. Output to `outputs/beat-breakdown-ep01.md`

### 3. Generate a Beat Board (9-Grid)

```
Please generate a beat board for ep01
```

The system will:

1. Storyboard Artist creates 9 prompts based on the approved breakdown
2. Apply the visual style and platform configuration
3. Director reviews consistency
4. Output to `outputs/beat-board-prompt-ep01.md`

#### 9-Grid Demo Result

![9-Grid Demo Result](images/demo.jpeg)

### 4. Generate a Sequence Board (4-Panel)

```
Please generate a sequence board for ep01
```

The system will:

1. Storyboard Artist selects a key beat from the 9 beats
2. Expand it into a continuous 4-shot sequence
3. Director checks motion continuity and axis rules
4. Output to `outputs/sequence-board-prompt-ep01.md`

### 5. Generate Motion Prompts

```
Please generate motion prompts for ep01
```

The system will:

1. Animator converts the 4-panel sequence into motion prompts
2. Optimize for video generation models
3. Director reviews physical plausibility
4. Output to `outputs/motion-prompt-ep01.md`

## Visual Style Configuration

The system supports multiple preset styles and platforms:

### Style Presets

**Photorealistic style**:

```
photorealistic, professional photography, cinematic lighting, high detail
```

**Anime style**:

```
anime style, soft cel shading, vibrant colors, expressive characters
```

**Concept art style**:

```
digital concept art, painterly style, dramatic atmosphere, detailed environment
```

### Supported Platforms

**Nano Banner** (default, recommended):

- 3x3 grid, generates all 9 beats in one pass
- Episode Visual Script format
- Visual Description (80-120 words) + Lighting & Mood (30-50 words)

![9-Grid Demo Result (Nano Banner)](images/demo.jpeg)

**Midjourney v6**:

- Independent prompts + parameters
- `--ar 16:9 --style cinematic --v 6`

**Gemini Imagen 3 / DALL-E 3**:

- Standard narrative descriptive prompts
- No special parameter requirements

## Core Methodology

### The Four Pillars (4C Framework)

1. **Clear**: Every prompt is unambiguous
2. **Concise**: Detailed but not bloated
   - Visual Description: 80-120 words
   - Lighting & Mood: 30-50 words
   - Motion Prompt: 40-80 words
3. **Consistent**: Character/scene/lighting stay consistent across all prompts
4. **Progressive**: Refine layer by layer from 9-grid → 4-panel, inheriting visual elements

### Layered Progressive Process

```
Beat Breakdown (9 anchors)
  ↓ inherits narrative structure
Beat Board (9-grid) — Establishes the visual baseline (character, scene, lighting and color)
  ↓ inherits visual elements
Sequence Board (4-panel) — Expands the action sequence, maintaining consistency
  ↓ inherits subject description
Motion Prompts — Converts to temporal, dynamic descriptions
```

## Key Constraints

### Character Consistency

**Canonical description** (established in Beat 1):

```
A young woman in her late 20s with waist-length straight silver hair,
pale porcelain skin, and bright violet eyes, wearing a long black coat
over a white high-neck shirt
```

**Repeat the key identifiers verbatim** in all subsequent beats:

- Hairstyle, hair color, hair length
- Eye color
- Main clothing
- Skin tone
- Distinguishing marks

### Output Purity

**Strictly prohibited** in output files:

- ❌ Frontmatter metadata (`---\nepisode: ep01\n---`)
- ❌ Template instructions or notes
- ❌ "Next step" directives
- ❌ Any non-prompt content

**Output only**: The actual prompt content itself

## Advanced Features

### Series Continuity

The Scriptwriter can review previous episodes and write sequels:

```
Based on ep01 and ep02, conceive a story about betrayal for ep03
```

The system will:

1. Read `script/ep01-*.md` and `script/ep02-*.md`
2. Analyze character development and unresolved plot threads
3. Create a new episode based on user input
4. Maintain character appearance and world-building consistency

### Professional Film Techniques

The system includes support for advanced film techniques:

**Montage**:

- Narrative Montage - Compresses time
- Thematic Montage - Contrasting juxtaposition
- Parallel Montage - Cross-cutting

**Transitions**:

- Cut, Match Cut, Dissolve
- Fade to Black, Smash Cut
- Each with guidance on when to use it

**Time and Space Manipulation**:

- Flashback - With visual indicators
- Dream Sequence
- Slow Motion
- Time Lapse
- Freeze Frame

### Quality Control

The Director automatically reviews every stage and delivers a PASS/FAIL verdict:

**Review criteria**:

- Correct beat count
- Clear, specific descriptions
- Consistent character appearance
- Complete shot specifications
- Physical plausibility
- No jump cuts or axis violations

**Revision loop**:

- FAIL → Storyboard Artist revises → Director re-reviews
- 3 consecutive FAILs → Escalate for Producer/user intervention

## Agent Architecture

### Producer (CLAUDE.md)

You (Claude) act as the Producer:

- Coordinate all sub-agents
- Understand user intent
- Schedule the workflow
- Handle escalations

### Scriptwriter

**Responsibilities**:

- Create structured scripts
- Review previous episodes to maintain continuity
- Conceive new stories based on user input
- Provide ≥9 beat candidates

**Skills**: `scriptwriter-skill`

### Storyboard Artist

**Responsibilities**:

- Identify 9 key beats from the script
- Generate 9-grid beat board prompts
- Generate 4-panel sequence board prompts
- Maintain character/scene/lighting consistency

**Skills**: `film-storyboard-skill`

### Director

**Responsibilities**:

- Review all outputs (beat breakdown, beat board, sequence board, motion prompts)
- Deliver PASS/FAIL verdicts
- Point out specific issues and suggested fixes
- Read-only, does not create

**Skills**: `storyboard-review-skill`

### Animator

**Responsibilities**:

- Convert 4-panel static sequences into motion prompts
- Optimize for AI video generation models
- Maintain subject consistency
- Ensure physically plausible motion

**Skills**: `animator-skill`

## Skill Architecture (2.0 Standardization)

All Skills have been refactored according to the [official Claude Code standard](https://code.claude.com/docs/en/skills), using the **progressive disclosure** pattern.

### film-storyboard-skill

**Core files**:

- `SKILL.md` (139 lines) - Overview, core principles, quick start, navigation
- `REFERENCE.md` 📖 - Platform features and style library (progressive disclosure)
  - Nano Banner vs Midjourney vs Gemini format comparison
  - Library of 7 visual styles (photorealistic, anime, concept art, etc.)
  - 6 candidate lighting schemes
  - Aspect ratio options
- `storyboard-methodology-playbook.md` 📖 - Complete methodology
- `gemini-image-prompt-guide.md` 📖 - Prompt writing guide
- `templates/` - Output templates

### scriptwriter-skill

**Core files**:

- `SKILL.md` (165 lines) - Overview, core principles, quick start, navigation
- `GUIDELINES.md` 📖 - Detailed writing guidelines (progressive disclosure)
  - Scene format specification
  - Character first-appearance rules
  - Beat distribution guidance
  - Dialogue writing techniques
- `templates/` - Output templates

### animator-skill

**Core files**:

- `SKILL.md` (225 lines) - Overview, core principles, quick start, navigation
- `MOTION_LIBRARY.md` 📖 - Complete motion library (progressive disclosure)
  - Subject motion library (character locomotion, actions, expressions)
  - Camera motion library (Pan, Dolly, Crane, Orbit)
  - Natural motion (wind, water, light and shadow)
  - Motion speed guidance
  - Platform features and optimization
- `motion-prompt-methodology.md` 📖 - Motion prompt methodology
- `templates/` - Output templates

### storyboard-review-skill

**Core files**:

- `SKILL.md` (68 lines) - Review philosophy and checklist references
- `review-checklist.md` - Detailed review criteria

## Technical Details

### File Naming Conventions

```
script/ep{XX}-{title}.md               # Script
outputs/beat-breakdown-ep{XX}.md       # Beat breakdown
outputs/beat-board-prompt-ep{XX}.md    # Beat board
outputs/sequence-board-prompt-ep{XX}.md # Sequence board
outputs/motion-prompt-ep{XX}.md        # Motion prompts
```

### Nano Banner 3x3 Grid

The 9 beats map to grid positions:

```
┌─────────┬─────────┬─────────┐
│ Beat 1  │ Beat 2  │ Beat 3  │
│ Top-L   │ Top-C   │ Top-R   │
├─────────┼─────────┼─────────┤
│ Beat 4  │ Beat 5  │ Beat 6  │
│ Mid-L   │ Center  │ Mid-R   │
├─────────┼─────────┼─────────┤
│ Beat 7  │ Beat 8  │ Beat 9  │
│ Bot-L   │ Bot-C   │ Bot-R   │
└─────────┴─────────┴─────────┘
```

### Prompt Language

- **Documentation, agent instructions, and metadata**: English (this repository was originally authored in Chinese and has been translated)
- **Actual AI prompt content**: English
  - Visual Description
  - Lighting & Mood
  - Motion Prompts

**Reason**: AI image/video models perform best with English prompts

## Example Output

### Beat Board (Nano Banner format)

```markdown
EPISODE 01: BEAT BOARD VISUAL SCRIPT

Beat 1: The Isolated Spark
Visual Description: Wide shot, high angle. A young woman in her late 20s
with waist-length straight silver hair, pale porcelain skin, and bright
violet eyes, wearing a long black coat over a white high-neck shirt, stands
alone on a crowded train platform. Commuters rush past her in blurred motion
while she remains perfectly still, staring at an ancient leather-bound journal
in her hands. Modern metropolitan subway station with fluorescent lighting
and yellow safety lines on the ground.
Lighting & Mood: Harsh overhead fluorescent lights creating flat, institutional
illumination. Cool blue-white color temperature. Isolated, contemplative
atmosphere with contrast between her stillness and surrounding chaos.

Beat 2: Crossing the Threshold
Visual Description: Medium shot, eye-level. The silver-haired woman in the
long black coat sits in a dimly lit subway car...
Lighting & Mood: Flickering cool fluorescent overhead light mixing with warm
amber glow from the journal pages...

[Continue Beat 3-9...]
```

### Motion Prompt

```markdown
Sequence 1 (based on Beat 1-2)

A woman with long silver hair in a black coat walks from left to right along
a train platform, wind blowing her hair gently. Other commuters move quickly
past in opposite direction. Camera static, eye-level. Steady walking pace,
contemplative mood. 5 seconds.
```

## Best Practices

### Writing High-Quality Scripts

1. **Visual first** - Describe with visualizable action, avoid abstract psychological description
2. **Character first appearance** - Provide a full appearance description
3. **Sufficient beats** - Ensure ≥9 clear key moments
4. **Three-act structure** - Setup (25%) → Confrontation (50%) → Resolution (25%), with 9 beats at the structural anchors (Hook, Inciting Event, First Plot Point, First Attempt, First Pinch Point, Midpoint, Third Plot Point, Climax, Resolution)

### Maintaining Consistency

1. **Establish the canon** - Fix character appearance in Beat 1
2. **Repeat verbatim** - Key identifiers are identical across all beats
3. **Inheritance rules** - The 4-panel sequence must inherit the visual elements of the source 9-grid
4. **Checklist** - Self-check against the Director's review criteria

### Optimizing Prompts

1. **Narrative descriptive** - Flowing sentences, not keyword stuffing
2. **Appropriate length** - Visual Description 80-120 words, Lighting & Mood 30-50 words
3. **Explicit shots** - Every prompt includes shot type and angle
4. **Lighting description** - Specify light source, direction, color temperature, atmosphere

## Troubleshooting

### Beat Board Consistency Issues

**Symptom**: Director reports inconsistent character appearance

**Fix**:

1. Check the canonical description in Beat 1
2. Make sure all beats use the same keywords
3. Verify that clothing, hairstyle, eye color, etc. match exactly

### Sequence Board Jump Cuts

**Symptom**: Director points out axis violations or jump cuts

**Fix**:

1. Check screen direction (180-degree rule)
2. Make sure shot type changes are clear
3. Add transition indicators (Cut, Dissolve, etc.)

### Motion Prompt Too Long

**Symptom**: Director reports more than 80 words

**Fix**:

1. Simplify the scene description
2. Focus on the motion itself
3. Remove excessive visual detail

## System Requirements

- Claude Code or claude.ai/code
- Workspace: local file system access
- No external dependencies

## License

This system is an internal tool; its methodology is based on publicly available film production standards.

## Contributing

Suggested improvements:

- New visual style presets
- Additional film technique documentation
- More template examples
- Platform-specific optimizations

---

**System version**: 2.0 (Skills standardization)
**Last updated**: 2026-01-11
**Agents**: 4 specialized sub-agents
**Skills**: 4 standardized skill packages (progressive disclosure pattern)
**Total Skills lines**: 607 lines (optimized -39.4%)
**Standards compliance**: 100% [official Claude Code standard](https://code.claude.com/docs/en/skills)
