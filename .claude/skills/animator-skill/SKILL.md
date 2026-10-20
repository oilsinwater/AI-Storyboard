---
name: animator-skill
description: Use when converting static image sequences (sequence boards) into motion prompts for AI video generation platforms (Runway, Pika, SVD), or describing temporal movement for video synthesis
version: 1.0.0
allowed-tools: Read, Write
user-invocable: false
---

# Animator Skill

Provides the Animator with the expertise to create dynamic motion prompts optimized for AI video generation workflows.

## Overview

This skill converts static 4-panel sequences into temporal motion descriptions, supporting:

- **Subject motion** - Character actions, expressions, poses
- **Camera motion** - Pan, Dolly, Crane, Orbit
- **Natural motion** - Wind, water, light and shadow
- **Platform optimization** - Runway Gen-3, Pika Labs, SVD, AnimateDiff

## Core Principles

### 1. Simplicity Over Complexity

**One primary action, not multiple simultaneous actions**

❌ **Too complex**:

```
Character runs forward, jumps over obstacle, spins mid-air, draws sword, lands in fighting stance
```

✅ **Focused and simple**:

```
Character runs forward and jumps over obstacle, landing in a crouch. Fast pace. 3 seconds.
```

### 2. Physical Plausibility

Duration must match the action:

- **3 seconds**: turn head, pick up object, take 2-3 steps
- **5 seconds**: cross a room, sit down/stand up, open a door and walk in
- **❌ Unrealistic**: "run 100 meters" in 3 seconds, "complete fight" in 5 seconds

### 3. Motion First, Details Second

Simplify the static description and emphasize motion:

❌ **Overly detailed** (120+ words):

```
A 25-year-old woman with waist-length silver hair, pale skin, violet eyes,
wearing black coat over white shirt and black pants, silver ring on right hand,
walks from left to right...
```

✅ **Motion first** (25 words):

```
A woman with silver hair in a black coat walks from left to right across platform.
Steady pace. 4 seconds.
```

### 4. Explicit Motion Source

State clearly what is moving:

- **Subject motion**: "Character walks left to right. Camera static."
- **Camera motion**: "Flower static. Camera pans right slowly."
- **Combined**: "Runner moves toward camera while camera dollies backward at matching speed."

## Motion Prompt Structure Template

```
[Simplified subject description] [primary action] [direction].
[Camera movement (if any)]. [Speed descriptor]. [Duration].
```

**Example**:

```
A woman with silver hair in a crimson coat walks from left to right along
a train platform, wind blowing her hair. Camera pans right to follow her.
Steady walking pace. 5 seconds.
```

## Quick Start

### Step 1: Analyze the Sequence Board

Identify the key motion in the 4-panel sequence:

- Frame 1 → Frame 2: what changed?
- Did the subject move? Did the camera move?
- Is there natural motion in the environment (wind, water, light)?

### Step 2: Choose One Primary Action

Do not try to describe every change; choose **the single most important one**.

### Step 3: Specify Direction

Use explicit directional vocabulary:

- left to right / right to left
- toward camera / away from camera
- background to foreground
- clockwise / counterclockwise

### Step 4: Choose Speed

Refer to the speed guidance in [MOTION_LIBRARY.md](MOTION_LIBRARY.md):

- **Slow** (4-5 seconds): slowly, gradually, gently
- **Medium** (3-4 seconds): walks, moves, steady pace
- **Fast** (2-3 seconds): quickly, swiftly, rushes

### Step 5: Determine Duration

According to platform and motion complexity:

- Runway Gen-3: 3-5 seconds
- Pika Labs: 3-4 seconds
- SVD: 2-4 seconds
- AnimateDiff: 1-3 seconds

## Output Constraints

**Strictly prohibited**:

- ❌ Frontmatter metadata
- ❌ Template instructions
- ❌ Verbose descriptions over 80 words
- ❌ Multiple competing actions
- ❌ Physically impossible motion

**Must include**:

- ✅ A concise 40-80 word description
- ✅ One clear primary action
- ✅ Motion direction
- ✅ Speed/pacing
- ✅ Duration
- ✅ Distinction between subject and camera motion

## Detailed Resources

### Methodology Guide 📖

- [motion-prompt-methodology.md](motion-prompt-methodology.md) - Motion prompt principles
  - Conciseness and focus
  - Specifying direction and speed
  - Distinguishing subject and camera motion
  - Physical plausibility for video durations
  - Video model optimization techniques

### Motion Type Library 📖

- [MOTION_LIBRARY.md](MOTION_LIBRARY.md) - Complete motion reference
  - Subject motion library (character locomotion, actions, expressions)
  - Camera motion library (Pan, Dolly, Crane, Orbit)
  - Natural motion (wind, water, light and shadow)
  - Motion speed guidance (slow/medium/fast)
  - Platform features and optimization (Runway, Pika, SVD, AnimateDiff)
  - Physical plausibility checks
  - Common motion combination examples

### Templates

- [templates/motion-prompt-template.md](templates/motion-prompt-template.md) - Output format

## When to Use

**Automatic trigger scenarios**:

- User requests "generate motion prompts"
- An approved sequence board needs to be converted to video
- Director feedback on motion clarity issues

**Manual reference scenarios**:

- Choosing an appropriate motion type
- Determining motion speed
- Optimizing platform-specific formats
- Checking physical plausibility

## Quick Platform Selection

- **Complex motion** → Runway Gen-3
- **Fast generation** → Pika Labs
- **Local deployment** → Stable Video Diffusion
- **Stylized animation** → AnimateDiff

## Common Mistakes and Fixes

### ❌ Mistake: Too verbose

```
(120+ words with excessive scene description)
```

✅ **Fix**: Simplify the scene, emphasize motion (~25 words)

### ❌ Mistake: Multiple actions

```
Character runs, jumps, spins, draws sword, lands
```

✅ **Fix**: Choose one primary action

### ❌ Mistake: Vague direction

```
Character moves around the room
```

✅ **Fix**: Make the direction explicit, e.g. "from background to foreground"

---

**Usage**: The Animator agent references this skill automatically. The methodology and library (marked 📖) use progressive disclosure and are consulted only when needed.
