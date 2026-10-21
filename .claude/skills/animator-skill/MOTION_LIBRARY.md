# Animator Skill - Motion Library

This document contains the complete motion type library, speed guidance, and platform feature reference. Consult only when choosing a motion type or optimizing platform output.

---

## Motion Type Library

### Subject Motion

#### Character Locomotion

```
walks from left to right
runs toward camera
turns slowly to face left
steps backward cautiously
walks diagonally across frame
approaches from background to foreground
exits frame left
```

#### Character Actions

```
reaches out with right hand
picks up object from table
opens door slowly
sits down in chair
stands up from seated position
points finger forward
waves hand in greeting
kneels down carefully
```

#### Expressions / Poses

```
head turns from left to right
smiles gradually
eyes widen in surprise
leans forward
tilts head questioningly
looks up slowly
nods in agreement
raises eyebrow
```

---

### Camera Motion

#### Pan

```
camera pans left to right
camera pans right to left following subject
horizontal pan across cityscape
```

#### Dolly

```
camera dollies forward toward subject
camera dollies backward revealing wider scene
slow dolly in on subject's face
dolly out from close-up to establishing shot
camera pushes in slowly
```

#### Crane/Boom

```
camera rises slowly upward
camera descends from high angle to eye level
crane up revealing landscape
boom down to character level
vertical descent following falling object
```

#### Orbit

```
camera orbits around subject clockwise
camera circles subject from right to left
360-degree rotation around central subject
arc around object revealing different angles
```

#### Other Camera Movements

```
camera tilts up from feet to face
camera tilts down from face to hands
slow tilt upward revealing environment
camera tilts down from sky to ground
camera zooms in slowly
camera zooms out revealing context
handheld camera movement, slight shake
tracking shot following character
static camera, no movement
```

---

### Natural Motion

#### Wind

```
wind blows hair gently to the right
leaves flutter in breeze
coat billows in strong wind
curtains sway in wind
dust particles drift in air current
flag waves vigorously
```

#### Water

```
water ripples expand outward
waves lap against shore
rain falls steadily
droplets run down window
water drips from ceiling
stream flows gently
```

#### Light and Shadow

```
shadows lengthen gradually
light flickers across face
sunbeams stream through window
shadow moves across wall
light fades to darkness
sun rays pierce through clouds
```

#### Other Natural Elements

```
snow falls softly
fire flickers and dances
smoke rises slowly
clouds drift across sky
fog rolls in gradually
petals fall from tree
```

---

## Motion Speed Guidance

### Slow-Paced Motion (Slow, Gradual)

**Keywords**:

- slowly
- gradually
- gently
- softly
- drifts
- eases
- creeps
- lingers

**Suitable for**:

- Emotionally delicate moments
- Building suspense
- Beauty shots
- Soft transitions
- Contemplative atmosphere

**Duration**: 4-5 seconds

**Examples**:

```
A woman slowly turns her head toward the window. Gentle, deliberate movement.
5 seconds.
```

---

### Medium Motion (Normal, Steady)

**Keywords**:

- walks
- moves
- turns
- steady pace
- normal speed
- regular motion
- consistent rhythm

**Suitable for**:

- Everyday actions
- Narrative progression
- Standard shots
- Naturalistic pacing
- Natural dialogue scenes

**Duration**: 3-4 seconds

**Examples**:

```
A man walks across the room from left to right, picking up a book from the table.
Steady walking pace. 4 seconds.
```

---

### Fast-Paced Motion (Fast, Sudden)

**Keywords**:

- quickly
- swiftly
- rapidly
- rushes
- darts
- sudden
- bursts
- snaps

**Suitable for**:

- Action scenes
- Jump-scare moments
- Sense of urgency
- Chase sequences
- Sudden reactions

**Duration**: 2-3 seconds

**Examples**:

```
A detective suddenly turns around, eyes wide, hand reaching for weapon.
Quick, sharp movement. 2 seconds.
```

---

## Supported Video Platforms

### Runway Gen-3 (Recommended)

**Strengths**:

- Supports complex motion
- High-quality output (1080p+)
- Good physical consistency
- Supports many motion types

**Best duration**: 3-5 seconds
**Recommended motion**: Complex camera motion + subject motion combinations

**Optimization tips**:

- Specify camera movement explicitly
- Avoid too many simultaneous motions
- Use directional descriptions (left to right, toward camera)

---

### Pika Labs

**Strengths**:

- Fast generation
- Suited to simple motion
- Easy to use
- Good coherence

**Best duration**: 3-4 seconds
**Recommended motion**: Single subject motion or simple camera pans

**Optimization tips**:

- Keep motion simple and focused
- Clear start and end states
- Avoid complex multi-layered motion

---

### Stable Video Diffusion (SVD)

**Strengths**:

- Open source and free
- Can be deployed locally
- Suited to subtle motion
- Strong community support

**Best duration**: 2-4 seconds
**Recommended motion**: Subtle expression changes, slight camera movement

**Optimization tips**:

- Focus on fine-detail motion
- Avoid large-scale actions
- Make use of static backgrounds

---

### AnimateDiff

**Strengths**:

- Integrates with Stable Diffusion
- Stylized animation
- Strong community support
- Highly controllable

**Best duration**: 1-3 seconds
**Recommended motion**: Stylized actions, artistic motion

**Optimization tips**:

- Make use of motion modules
- Maintain style consistency
- Suited to non-photorealistic animation

---

## Motion Combination Patterns

### Static Subject + Camera Motion

```
Flower stands still in center of frame. Camera orbits around it clockwise.
Smooth steady rotation. 5 seconds.
```

**Suitable for**: Product showcases, aesthetic shots, establishing environments

---

### Moving Subject + Static Camera

```
Runner sprints from left to right across frame. Camera static, wide shot.
Fast running pace. 3 seconds.
```

**Suitable for**: Action sequences, chase scenes, showcasing movement

---

### Synchronized Motion (Tracking Shot)

```
Athlete runs toward camera while camera dollies backward at matching speed,
maintaining consistent distance. Medium running pace. 4 seconds.
```

**Suitable for**: Walk-and-talk dialogue, chase scenes, dynamic action

---

### Contrasting Motion

```
Character walks slowly left to right in foreground while camera pans right
to left, creating parallax effect. Slow walking, steady pan. 5 seconds.
```

**Suitable for**: Artistic shots, visual depth, emotional expression

---

## Physical Plausibility Check

### Matching Duration to Action

**Actions suited to 3 seconds**:

- Turn head 90 degrees
- Pick up an object from a table
- Take 2-3 steps
- Expression changes to a smile
- Simple gesture

**Actions suited to 5 seconds**:

- Cross a small room
- Sit down or stand up
- Open a door and walk in
- Turn and walk away
- Camera orbits 180 degrees

**❌ Unrealistic combinations**:

- "Character runs 100 meters" in 3 seconds (human limit ~9 seconds)
- "Complete fight sequence" in 5 seconds
- "Car accelerates from standstill to high speed" in 2 seconds

---

## Common Motion Combination Examples

### Emotional Turning Point

```
Character standing still, slowly looks up, eyes widen in realization.
Camera static. Gradual expression change. 4 seconds.
```

### Discovery / Reveal

```
Camera dollies forward toward mysterious box on table. Box static.
Slow steady dolly. 5 seconds.
```

### Establishing the Environment

```
Camera pans left to right across cityscape at sunset. Static buildings,
moving clouds. Smooth steady pan. 5 seconds.
```

### Confrontation / Conflict

```
Two characters walk toward each other from opposite sides of frame,
stopping face to face. Camera static. Steady walk. 4 seconds.
```

### Departure / Ending

```
Character walks away from camera toward door in background. Camera static.
Slow walking pace. 5 seconds.
```

---

## Usage Recommendations

1. **Determine the primary motion first** - Subject motion or camera motion?
2. **Choose the speed** - Slow/medium/fast, matching the emotion
3. **Check the duration** - Can the motion be completed within the specified duration?
4. **Refer to platform features** - Does the chosen platform support this level of complexity?
5. **Simplify the description** - Remove details unrelated to motion

---

**Maintenance note**: This library is updated periodically according to the capabilities of mainstream AI video platforms.
