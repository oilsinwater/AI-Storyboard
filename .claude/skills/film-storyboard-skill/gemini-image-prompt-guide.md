# 📖 Nano Banner Prompt Writing Guide (Reference Only)

> **Note**: This is a reference guide. **Consult only when you have questions about the Nano Banner prompt format**.
> **Do not load this file automatically** - refer to it only when confused or when needed.

---

# Nano Banner Prompt Guide

A prompt writing guide optimized specifically for Nano Banner 3x3 grid generation.

**Important notes**:

- This guide focuses on the **Nano Banner Episode Visual Script format**
- The Nano Banner format is **different** from the standard Gemini/Midjourney format
- Prompt content is **written in English** for the best generation results
- This is a 📖 **Reference Only** document and is not loaded into context automatically

---

## Nano Banner Core Format

### Episode Visual Script Structure

Nano Banner uses a special "Episode Visual Script" format, optimized for generating the complete 3x3 grid in one pass:

```markdown
EPISODE {XX}: BEAT BOARD VISUAL SCRIPT

Beat 1: [Beat title]
Visual Description: [80-120 word detailed visual description]
Lighting & Mood: [30-50 words on lighting and atmosphere]

Beat 2: [Beat title]
Visual Description: [80-120 word detailed visual description]
Lighting & Mood: [30-50 words on lighting and atmosphere]

[Continue Beat 3-9, 9 beats in total]
```

### Format Requirements

**Title line**:

```
EPISODE {XX}: BEAT BOARD VISUAL SCRIPT
```

- Must include the episode number
- Fixed format, cannot be omitted

**Structure of each Beat** (exactly 3 lines):

1. `Beat X: [Title]` - Beat number and title
2. `Visual Description:` - 80-120 word detailed visual description
3. `Lighting & Mood:` - 30-50 words on lighting and atmosphere

**Total**: 1 title line + 9 beats × 3 lines = 28 lines

### 3x3 Grid Layout

The 9 beats correspond to the nano banner 3x3 grid positions:

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

**Key points**:

- Nano banner renders these 9 beats simultaneously as a 3x3 grid
- Beats 1-3 are the first row (top)
- Beats 4-6 are the second row (middle)
- Beats 7-9 are the third row (bottom)
- Maintaining character/style consistency across all beats is critical

---

## Visual Description Writing Rules

### Required Elements (in order)

1. **Shot specification** (Shot Type + Angle)

   ```
   Wide shot, high angle.
   Medium shot, eye-level.
   Close-up, low angle.
   ```

2. **Character description** (Canonical Description)

   ```
   A young woman in her late 20s with waist-length straight silver hair,
   pale porcelain skin, and bright violet eyes, wearing a long black coat
   over a white high-neck shirt
   ```

   **Key**: All 9 beats must use **exactly the same** character description

3. **Action/pose**

   ```
   stands alone on a crowded platform
   sits in a dimly lit subway car, the journal open on her lap
   reaches toward a glowing object
   ```

4. **Scene setting**

   ```
   Modern metropolitan subway station with fluorescent lighting and
   yellow safety lines on the ground
   ```

   Include 2-4 distinctive scene features

5. **Key visual elements**
   ```
   Commuters rush past her in blurred motion while she remains perfectly still,
   staring at an ancient leather-bound journal in her hands
   ```

### Length Control

- **Optimal**: 80-120 words
- **Too short** (<60 words): Missing necessary detail
- **Too long** (>140 words): Information overload; nano banner may ignore parts

### Narrative Descriptive Style

❌ **Wrong** (keyword stuffing):

```
woman, silver hair, black coat, subway, neon, dramatic, 8k, detailed
```

✅ **Correct** (narrative description):

```
Wide shot, high angle. A young woman in her late 20s with waist-length straight
silver hair, pale porcelain skin, and bright violet eyes, wearing a long black
coat over a white high-neck shirt, stands alone on a crowded train platform.
Commuters rush past her in blurred motion while she remains perfectly still,
staring at an ancient leather-bound journal in her hands. Modern metropolitan
subway station with fluorescent lighting and yellow safety lines on the ground.
```

---

## Lighting & Mood Writing Rules

### Required Elements

1. **Light source and direction**

   ```
   Harsh overhead fluorescent lights creating flat, institutional illumination
   Warm golden sunlight streaming from the left
   Flickering cool fluorescent overhead light mixing with warm amber glow
   ```

2. **Light quality**

   ```
   Soft diffused natural light
   Dramatic high contrast lighting
   Rim lighting creating silhouette effect
   ```

3. **Color temperature**

   ```
   Cool blue-white color temperature
   Warm amber and orange tones
   Cold silvery moonlight
   ```

4. **Emotional atmosphere**
   ```
   Isolated, contemplative atmosphere
   Mysterious and tense mood
   Eerie, supernatural feeling
   ```

### Length Control

- **Optimal**: 30-50 words
- **Too short** (<20 words): Not specific enough
- **Too long** (>60 words): Belongs in the Visual Description instead

---

## Character Consistency Techniques

### Establishing the Canonical Description

Establish the full character description in Beat 1, then repeat the key identifiers **verbatim** in all 9 beats:

**Canonical description**:

```
A young woman in her late 20s with waist-length straight silver hair,
pale porcelain skin, and bright violet eyes, wearing a long black coat
over a white high-neck shirt
```

**Repeated in later beats**:

```
Beat 1: ...the silver-haired woman in her late 20s with violet eyes and
        a long black coat stands...

Beat 5: ...the same woman with waist-length silver hair and bright violet
        eyes, still wearing the long black coat, walks...

Beat 9: ...the young woman with silver hair and violet eyes in the black coat...
```

### Key Identifiers

Must remain consistent across all beats:

- Hairstyle, hair color, hair length
- Eye color
- Main clothing (coat, dress, etc.)
- Skin tone
- Distinguishing marks (scars, tattoos, etc.)

---

## Complete Example

```markdown
EPISODE 01: BEAT BOARD VISUAL SCRIPT

Beat 1: The Isolated Spark
Visual Description: Wide shot, high angle. A young woman in her late 20s with waist-length straight silver hair, pale porcelain skin, and bright violet eyes, wearing a long black coat over a white high-neck shirt, stands alone on a crowded train platform. Commuters rush past her in blurred motion while she remains perfectly still, staring at an ancient leather-bound journal in her hands. Modern metropolitan subway station with fluorescent lighting and yellow safety lines on the ground.
Lighting & Mood: Harsh overhead fluorescent lights creating flat, institutional illumination. Cool blue-white color temperature. Isolated, contemplative atmosphere with contrast between her stillness and surrounding chaos.

Beat 2: Crossing the Threshold
Visual Description: Medium shot, eye-level. The silver-haired woman in the long black coat sits in a dimly lit subway car, the journal open on her lap. Her violet eyes are narrowed as she studies a page filled with hand-drawn symbols and glowing six-pointed star diagrams. The fluorescent lights flicker above. Other passengers visible in soft focus in the background, unaware of the otherworldly glow emanating from the pages.
Lighting & Mood: Flickering cool fluorescent overhead light mixing with warm amber glow from the journal pages. Creates an eerie, supernatural mood. Mysterious and tense atmosphere.

Beat 3: The Hidden Message
Visual Description: Close-up, slightly high angle. The open journal fills the frame, showing intricate hand-drawn diagrams, cryptic symbols in an unknown language, and a central six-pointed star radiating soft golden light. The woman's pale hands with delicate fingers hold the edges of the pages. Aged paper texture visible, with slight yellowing and worn edges indicating the journal's antiquity.
Lighting & Mood: Warm golden glow radiating from the star diagram, illuminating the aged paper. Soft ambient light from above creates gentle shadows. Mystical, ancient atmosphere with hints of magic.

Beat 4: The First Sign
Visual Description: Medium shot, low angle. The young woman with waist-length silver hair and violet eyes, still wearing the long black coat, stands at the subway door as it opens. She looks up sharply, her expression shifting from concentration to alert awareness. Through the open door, a swirling vortex of purple and blue energy is visible instead of the normal platform. Other passengers continue moving normally, oblivious.
Lighting & Mood: Cool fluorescent car interior lighting contrasts with vibrant purple-blue ethereal glow from the vortex. Heightened tension and anticipation. Supernatural energy becoming visible.

Beat 5: Stepping Into the Unknown
Visual Description: Full shot, eye-level. The silver-haired woman in her black coat steps through the subway doorway toward the swirling energy vortex. Her right foot crosses the threshold while her left remains in the car. Her silver hair begins to float and swirl as if caught in an invisible wind. The journal is clutched tightly to her chest. Reality appears to distort around the doorway, with warped perspective and bending light.
Lighting & Mood: Dramatic contrast between flat subway lighting and the dynamic, swirling purple-blue glow of the portal. Hair-raising, momentous atmosphere. Point of no return energy.

Beat 6: The In-Between
Visual Description: Wide shot, Dutch angle. The woman with silver hair and violet eyes floats in a vast void of swirling purple, blue, and silver energy streams. The black coat billows around her as if underwater. Fragments of reality—pieces of the subway, glimpses of strange otherworldly architecture—float past in the background. She holds the glowing journal close, its light creating a protective sphere around her.
Lighting & Mood: Ethereal, omnidirectional glow from energy streams in purple and blue hues. The journal's warm golden light provides a safe anchor point. Surreal, dreamlike yet slightly unsettling atmosphere.

Beat 7: Arrival
Visual Description: Medium shot, low angle. The young woman with waist-length silver hair and bright violet eyes in the long black coat emerges from a doorway of light into a vast ancient library with impossibly tall bookshelves reaching into darkness above. Thousands of leather-bound books line the shelves. Floating candles provide illumination. She stands in the center, looking around in wonder and apprehension, journal still in hand.
Lighting & Mood: Warm golden candlelight from hundreds of floating candles creates dancing shadows. Mixture of welcoming warmth and mysterious darkness in the unreachable upper shelves. Ancient, magical atmosphere filled with hidden knowledge.

Beat 8: The Revelation
Visual Description: Close-up, eye-level. The woman's face fills the frame, her bright violet eyes wide with realization and fear. Her pale skin is illuminated by the warm glow of candlelight from below, creating dramatic upward shadows. Silver hair frames her face. Over her shoulder, blurred in the background, shelves of ancient books are visible. Her expression conveys the weight of understanding something profound and dangerous.
Lighting & Mood: Dramatic upward lighting from candles below creates shadows under her eyes and cheekbones. Warm golden-orange color temperature. Tense, revelatory mood mixing awe with creeping dread.

Beat 9: Acceptance of Destiny
Visual Description: Wide shot, high angle. The young woman with silver hair and violet eyes in the long black coat walks determinedly down a long corridor between towering bookshelves, journal held at her side. Floating candles light her path. Her shadow stretches long behind her. Ancient stone floor beneath her feet. The perspective creates a sense of journey and purpose. She's small against the vast library but moving forward with resolve.
Lighting & Mood: Warm candlelight creating a path forward while darkness looms on either side. Long dramatic shadows emphasizing her solitary journey. Determined, resolute atmosphere with underlying tension of the unknown ahead.
```

---

## Common Mistakes

### ❌ Inconsistent character description

```
Beat 1: woman with long silver hair
Beat 5: woman with short blonde hair
```

**Problem**: Nano Banner will generate two people with different appearances

### ❌ Too short

```
Visual Description: A woman stands in a train station. (7 words)
```

**Problem**: Not enough information; nano banner cannot generate a detailed image

### ❌ Keyword stuffing

```
Visual Description: woman, silver hair, black coat, subway, mysterious, 8k, cinematic, detailed
```

**Problem**: Nano Banner needs narrative description, not keyword lists

### ❌ Missing shot specification

```
Visual Description: A woman with silver hair stands on a platform...
```

**Problem**: Missing shot information such as "Wide shot, high angle"

### ❌ Lighting & Mood too long

```
Lighting & Mood: The lighting consists of harsh overhead fluorescent lights that
create a very flat and institutional type of illumination with a cool blue-white
color temperature, and the overall mood is one of isolation and contemplation,
with a strong contrast between her stillness and the chaos of the surrounding
commuters rushing past... (65 words)
```

**Problem**: Exceeds the 50-word limit; should be moved into the Visual Description

---

## Quality Self-Check

**Per-beat checks**:

- [ ] Visual Description: 80-120 words
- [ ] Lighting & Mood: 30-50 words
- [ ] Includes shot type and angle
- [ ] Character description is consistent with Beat 1
- [ ] Uses narrative descriptive style (not keywords)
- [ ] Scene includes 2-4 distinctive features
- [ ] Light source, direction, and color temperature are specified
- [ ] Emotional atmosphere is described

**Overall checks**:

- [ ] Exactly 9 beats
- [ ] Title line format is correct: "EPISODE XX: BEAT BOARD VISUAL SCRIPT"
- [ ] Character appearance is 100% consistent across all beats
- [ ] No frontmatter or metadata
- [ ] No template instructions or notes

---

This guide is optimized specifically for Nano Banner 3x3 grid generation. Following these rules ensures the 9 generated panels have visual consistency and professional quality.
