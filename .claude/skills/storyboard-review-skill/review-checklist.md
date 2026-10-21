# Storyboard Review Checklist

Comprehensive quality standards for the output of each production stage.

---

## Stage 1: Beat Breakdown Review

**Artifact**: `beat-breakdown-ep{XX}.md`

### Count and Completeness

- [ ] **Exactly 9 beats** (not 8, not 10, exactly 9)
- [ ] All 9 beats have a **beat number** (1-9)
- [ ] All 9 beats have a **scene reference** (page number, scene number, or timestamp)
- [ ] All 9 beats have a **description** (not blank or a placeholder)
- [ ] All 9 beats have a **narrative purpose** (explaining why this beat matters)

### Coverage and Distribution

- [ ] **Act One covered**: Beats 1-3 are the Hook / Characteristic Moment, the Inciting Event, and the First Plot Point (the protagonist's choice that sets the goal)
- [ ] **Act Two covered**: Beats 4-7 are the First Attempt, the First Pinch Point, the Midpoint, and the Third Plot Point (the low point)
- [ ] **Act Three covered**: Beats 8-9 are the Climax and the Resolution
- [ ] **Anchored spacing**: Beats follow the structural anchors (not all clustered, not spaced by equal page gaps)
- [ ] **Complete arc**: The 9 beats together tell a complete story

### Clarity and Specificity

- [ ] **No vague descriptions**: Each beat describes a specific event
  - ❌ Fail: "Something happens to the character"
  - ✓ Pass: "Maya discovers a hidden map in her grandmother's diary"
- [ ] **Concrete action**: Descriptions use active, tangible events
- [ ] **Understandable on its own**: Each beat can be understood without extensive context

### Selection Quality

- [ ] **Turns**: Each beat changes the character's emotional state; no incidents without a turn
- [ ] **Visual potential**: Each beat can be represented by a compelling image with at most three characters
- [ ] **Story-essential**: Removing any beat would leave a gap; the Purpose names the anchor's job
- [ ] **Emotional significance**: Beats carry structural emotion (curiosity, anticipation, surprise) or thematic emotion (sympathy, identification, empathy); setbacks outnumber good news
- [ ] **Promises kept**: Anything planted in an early beat pays off in a later one

### Character and Location Tracking

- [ ] **Key characters listed**: All recurring characters are identified with canonical descriptions
- [ ] **Key locations listed**: All recurring settings are identified
- [ ] **Consistency foundation**: Enough information is provided to maintain continuity in later stages

### Common Failure Patterns

- ❌ Wrong beat count (7, 10, 12 beats instead of exactly 9)
- ❌ Vague descriptions ("a scene", "something happens", "the character does things")
- ❌ Missing anchors (e.g. no Climax, no First Plot Point, no Midpoint)
- ❌ Mundane moments (beats describing unimportant actions, or moments with no turn)
- ❌ Clustered beats (all 9 beats in the first third of the story)

---

## Stage 2: Beat Board (9-Grid) Review

**Artifact**: `beat-board-prompt-ep{XX}.md`

### Count and Structure

- [ ] **Exactly 9 prompts** (one per beat, from the breakdown)
- [ ] Each prompt has a **beat reference** (citing the corresponding beat in the breakdown)
- [ ] Each prompt has **narrative context** (explaining what is happening)

### Prompt Format and Style

- [ ] **Narrative descriptive style**: Flowing sentences, not keyword lists
  - ❌ Fail: "woman, red dress, beach, sunset, 8k, detailed"
  - ✓ Pass: "A woman in a red dress stands on a beach at sunset..."
- [ ] **Appropriate length**: 80-150 words per prompt
  - Too short (<60 words) → missing detail
  - Too long (>180 words) → bloated, unfocused
- [ ] **Shot specification**: Each prompt includes shot type and camera angle
  - Required: "Medium shot, eye-level" or similar wording

### Clarity (C1 of the 4C Framework)

- [ ] **Subject clearly defined**: No ambiguity about who/what the main subject is
- [ ] **Action/pose specified**: The subject's position and action are described
- [ ] **Scene detailed**: The location includes 2-4 distinctive features
- [ ] **Lighting described**: Direction, quality, and atmosphere of the lighting are specified
- [ ] **No contradictions**: Elements do not conflict (e.g. "bright sunshine in a dark room")

### Consistency (C3 of the 4C Framework)

- [ ] **Character appearance identical**: The same character is described identically across all prompts
  - Example check: If Prompt 1 says "long silver hair", Prompt 5 must also say "long silver hair"
  - Look for: hair, eyes, clothing, distinguishing marks
- [ ] **Scene consistency**: If a location appears in multiple prompts, the details align
- [ ] **Style keywords uniform**: All prompts use the same style markers
  - Example: If Prompt 1 uses "anime style, cinematic lighting", all prompts should
- [ ] **Lighting approach coherent**: The overall lighting concept is maintained (unless the story requires a change)

### Coverage and Alignment

- [ ] **Beats match the breakdown**: Each panel corresponds to the correct beat from Stage 1
- [ ] **Visual storytelling**: The 9 panels together tell the episode's story visually
- [ ] **Shot variety**: A mix of wide, medium, and close-up shots (not all the same shot type)

### Style Marker Application

- [ ] **Project style applied**: The visual style from the project configuration is used in all prompts
- [ ] **Aspect ratio noted**: Specified in the metadata (e.g. 16:9, 1:1)
- [ ] **Target model noted**: The AI model is identified (e.g. Gemini Imagen 3)

### Common Failure Patterns

- ❌ Wrong prompt count (8 or 10 prompts instead of 9)
- ❌ Keyword stuffing ("detective, noir, rain, night, trench coat, fedora, 8k, detailed")
- ❌ Character inconsistency (Prompt 2 has "short black hair" but Prompt 7 has "long blonde hair")
- ❌ Missing shot specification (no mention of shot type or camera angle)
- ❌ Vague descriptions ("a person in a place")
- ❌ Style keywords missing or inconsistent between prompts

---

## Stage 3: Sequence Board (4-Panel Sequence) Review

**Artifact**: `sequence-board-prompt-ep{XX}.md`

### Structure and Count

- [ ] **Exactly 4 panels per sequence** (not 3, not 5)
- [ ] **Source beat identified**: Each sequence references its source in the beat board
- [ ] **Narrative context provided**: What happens across the 4 panels is explained
- [ ] **Estimated duration**: Real-time duration is noted (e.g. "8 seconds")

### Inheritance (Critical)

- [ ] **Character appearance inherited**: Panels use the same character description as the source beat
  - Cross-check: Does Panel 1's character description match Beat X's description?
  - Example: If Beat 5 says "woman with curly red hair in a blue jacket", all 4 panels must maintain this
- [ ] **Scene inherited**: The location matches or logically extends from the source beat
- [ ] **Lighting inherited**: The lighting approach is consistent with the source beat (unless the story requires a change)

### Action Continuity

- [ ] **Logical progression**: Action flows naturally from Panel 1 → 2 → 3 → 4
- [ ] **Physically possible**: The action can occur within the estimated duration
  - ❌ Fail: "Character runs 100 meters" in 3 seconds
  - ✓ Pass: "Character takes 3 steps forward" in 3 seconds
- [ ] **No teleporting**: Characters/objects move through space, not jump positions
- [ ] **Clear transitions**: Transitions between panels are specified (cut, pan, push, etc.)

### Cinematography (180-Degree Rule)

- [ ] **Screen direction maintained**: Characters do not flip positions without reason
  - Example: If Character A is on the left in Panel 1, they should remain on the left in Panels 2-4 unless they physically move
- [ ] **Axis stability**: The imaginary line between subjects is maintained
- [ ] **Line crossing justified**: If the 180-degree line is crossed, it is shown (not jumped)

### Edit Safety (Avoiding Jump Cuts)

- [ ] **No jump cuts**: Avoid the same shot at a slightly different angle
  - ❌ Fail: Panel 1: "Medium shot of character", Panel 2: "Medium shot of character, camera slightly closer"
  - ✓ Pass: Panel 1: "Medium shot", Panel 2: "Close-up of character's face" (clear change)
- [ ] **Clear shot changes**: When cutting, shot type or angle changes significantly
- [ ] **Smooth transitions**: Cuts are motivated and clear, not jarring

### Panel Prompt Quality

- [ ] **80-150 words per panel**: Appropriate length maintained
- [ ] **Narrative descriptive style**: Not keyword lists
- [ ] **Includes shot specification**: Shot type, camera angle, transition type

### Sequence Pacing

- [ ] **Action fits the duration**: The described motion can realistically be completed in the time
- [ ] **Pacing variety**: Not all sequences are the same speed (some slow, some fast)
- [ ] **Camera movement clear**: If the camera moves, direction and type are specified

### Common Failure Patterns

- ❌ Wrong panel count per sequence (3 or 5 panels instead of 4)
- ❌ Character appearance differs from the source beat (inheritance violation)
- ❌ Screen direction violation (character switches from left to right with no motion)
- ❌ Jump cuts (Panel 1 medium shot, Panel 2 slightly different medium shot)
- ❌ Impossible action (character flies across the room in 1 second, no superpowers)
- ❌ Unclear transitions (no indication of how Panel 1 connects to Panel 2)
- ❌ Unexpected scene change (Panel 1 in an office, Panel 3 suddenly in a forest, no explanation)

---

## Stage 4: Motion Prompt Review

**Artifact**: `motion-prompt-ep{XX}.md`

### Structure and Count

- [ ] **One prompt per sequence**: Each 4-panel sequence gets one motion prompt
- [ ] **Source sequence identified**: References which sequence it is based on
- [ ] **Duration specified**: Target video duration is noted (typically 3-5 seconds)

### Conciseness (Critical for Video Models)

- [ ] **Appropriate length**: 40-80 words (significantly shorter than static prompts)
  - Too long (>100 words) → the model may ignore parts
  - Too short (<30 words) → missing necessary detail
- [ ] **Focused description**: Describes motion, not exhaustive scene detail
  - ❌ Fail: "In a beautifully lit Victorian room with ornate furniture, tall windows, red velvet curtains..."
  - ✓ Pass: "In a Victorian room,..."

### Motion Clarity

- [ ] **Primary motion defined**: One clear primary action is described
  - ❌ Fail: "Character runs, jumps, spins, waves, while camera zooms and pans"
  - ✓ Pass: "Character runs forward, camera pans left to follow"
- [ ] **Direction specified**: Motion direction is explicit and unambiguous
  - Required: "left to right", "toward camera", "clockwise", etc.
  - ❌ Fail: "Character moves"
  - ✓ Pass: "Character moves from left to right"
- [ ] **Speed indicated**: The pacing of the motion is clear
  - Use: "slowly", "quickly", "drifting", "sprinting", etc.

### Subject vs Camera Motion

- [ ] **Motion source clear**: Specifies what is moving (subject, camera, or both)
  - "Character walks forward" (subject moves)
  - "Camera dollies backward" (camera moves)
  - "Character runs left, camera pans right" (both move)
- [ ] **Camera movement specified**: If the camera moves, the type is clear
  - Pan, tilt, dolly, truck, zoom, orbit

### Physical Plausibility

- [ ] **Duration realistic**: The motion can be completed in the stated time
  - 3 seconds: simple actions (turn head, pick up object, take a step)
  - 5 seconds: moderate actions (cross a small room, sit down, open a door)
  - ❌ Fail: "Character runs a marathon" in 3 seconds
- [ ] **Obeys physics**: No impossible motion (unless supernatural/justified)

### Subject Consistency

- [ ] **Character description matches the source**: Subject described as in the sequence board
  - A full exhaustive description is not needed, but key identifiers are maintained
  - Example: If the sequence has "silver-haired woman in a red coat", the motion prompt should include these identifiers

### Focus and Conciseness

- [ ] **Single primary action**: Not multiple competing motions
- [ ] **Essential detail only**: Background is simplified compared to static prompts
- [ ] **Motion-centered**: Emphasizes movement, not static composition

### Common Failure Patterns

- ❌ Too verbose (120+ words, reads like a static image prompt)
- ❌ Multiple competing motions ("runs, jumps, spins, waves, turns")
- ❌ Vague direction ("character moves around")
- ❌ Impossible timing ("character runs across the city" in 3 seconds)
- ❌ Character description does not match the sequence board
- ❌ Motion direction unspecified
- ❌ Unclear what is moving (subject? camera? both?)

---

## Review Output Format

When conducting a review, the Director should structure feedback as follows:

```markdown
## Review: [Artifact Name]

**Stage**: [1, 2, 3, or 4]
**Verdict**: PASS | FAIL

### Quality Check Results:

- [ ] Criterion 1: PASS/FAIL - [brief note]
- [ ] Criterion 2: PASS/FAIL - [brief note]
- [ ] Criterion 3: PASS/FAIL - [brief note]
      [...continue for all relevant criteria...]

### Issues Found:

[If FAIL, list specific issues with references to beats/prompts/panels]

1. **Issue**: [description]

   - **Location**: [Beat 5, Prompt 3, Panel 2, etc.]
   - **Problem**: [specific explanation]
   - **Fix Required**: [what needs to change]

2. **Issue**: [...]

### Recommended Actions:

[If FAIL, provide step-by-step revision guidance]

### Approval Notes:

[If PASS, optionally note what was done well or minor suggestions]
```

---

## Decision Matrix

### When to PASS:

- ✓ All **major criteria** are met
- ✓ Minor issues are cosmetic only (e.g. typos that do not affect generation)
- ✓ The work is ready for AI generation
- ✓ The methodology principles (clear, concise, consistent, progressive) are demonstrated

### When to FAIL:

- ✗ Any **major criterion** is violated
- ✗ Consistency issues (character appearance changes, screen direction violations)
- ✗ Missing required elements (no shot specification, no lighting description)
- ✗ Methodology violations (keyword format instead of narrative, wrong length)
- ✗ Safety issues (continuity errors, jump cuts in sequences)
- ✗ Inheritance failures (4-panel does not match the source 9-grid)

**Important**: When in doubt, FAIL and request clarification. Ensuring quality now is always better than wasting generation resources on flawed prompts.

---

## Revision Loop Limits

- **Normal flow**: FAIL → revise → review → PASS
- **After 3 consecutive FAILs on the same artifact**: Escalate to the Producer for user intervention
  - May indicate: unclear requirements, technical misunderstanding, or the need for user input

---

This checklist is the foundation of quality control for the entire storyboard production system.
