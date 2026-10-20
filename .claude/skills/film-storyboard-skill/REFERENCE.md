# Film Storyboard Skill - Platform & Style Reference

This document contains platform features, the visual style library, and technical reference. Consult only when needed.

---

## Platform Support

### Nano Banner (Default, Recommended)

**Format**: Episode Visual Script mode

- 9 beats, each containing Visual Description + Lighting & Mood
- Optimized for nano banner 3x3 grid generation
- Generates the complete 9-grid in a single pass, guaranteeing consistency

**Format Specification**:

```markdown
EPISODE {XX}: BEAT BOARD VISUAL SCRIPT

Beat 1: [Beat title]
Visual Description: [Shot type]. [Canonical character description] [action/pose] [scene details] [key visual elements]. [80-120 words]
Lighting & Mood: [Light direction, quality, color temperature] [emotional atmosphere]. [30-50 words]

Beat 2: [Beat title]
Visual Description: ...
Lighting & Mood: ...

[Continue Beat 3-9]
```

### Midjourney v6

**Format**: Independent prompts + parameters

- One independent prompt per beat
- Includes the `--ar 16:9 --style cinematic --v 6` parameters
- Grid position labeled

**Example**:

```
Beat 1 (Grid Position: Top-Left):
[Prompt content]
--ar 16:9 --style cinematic --v 6
```

### Gemini Imagen 3 / DALL-E 3

**Format**: Standard narrative descriptive prompts

- No special parameter requirements
- Relies on detailed narrative description
- 80-150 words per beat

---

## Visual Style Library

### Recommended Style Combinations

#### Photorealistic Style

```
photorealistic, professional photography, cinematic lighting, high detail
```

**Suitable for**: Contemporary drama, documentary style, live-action film

#### Anime Style

```
anime style, soft cel shading, vibrant colors, expressive characters
```

**Suitable for**: Japanese animation, manga adaptations, coming-of-age stories

#### Concept Art Style

```
digital concept art, painterly style, dramatic atmosphere, detailed environment
```

**Suitable for**: Fantasy worlds, sci-fi settings, game-like narratives

#### Film Noir Style

```
film noir aesthetic, high contrast black and white, dramatic shadows, moody atmosphere
```

**Suitable for**: Mystery, crime, retro detective stories

#### Cyberpunk Style

```
cyberpunk aesthetic, neon lighting, rain-slicked streets, vibrant pink and cyan colors
```

**Suitable for**: Future cities, tech dystopias, nighttime urban settings

#### Fantasy Illustration Style

```
fantasy illustration style, painterly, rich colors, epic composition
```

**Suitable for**: Magical worlds, epic adventures, fairy tale adaptations

#### Watercolor Style

```
watercolor painting style, soft edges, flowing colors, artistic paper texture
```

**Suitable for**: Heartwarming stories, memory scenes, poetic narratives

---

## Candidate Lighting Schemes

### Golden Hour

```
warm golden hour sunlight, long soft shadows, orange and amber tones
```

**Mood**: Warm, nostalgic, hopeful

### Blue Hour

```
cool blue twilight, soft gradient from purple to dark blue, minimal shadows
```

**Mood**: Tranquil, mysterious, transitional

### Cinematic Lighting

```
cinematic lighting, dramatic contrast, three-point lighting setup
```

**Mood**: Dramatic, professional, classic

### Soft Natural Light

```
soft diffused natural light, even illumination, gentle shadows
```

**Mood**: Calm, authentic, everyday

### Neon Night

```
vibrant neon lighting in pink and cyan, colored reflections, high contrast
```

**Mood**: Futuristic, urban, energetic

### Dramatic Side Lighting

```
dramatic side lighting, split lighting effect, deep shadows
```

**Mood**: Conflict, tension, opposition

---

## Aspect Ratio Options

- **16:9** - Widescreen cinematic (recommended, mainstream video platforms)
- **1:1** - Square (Instagram posts)
- **9:16** - Vertical (TikTok, Reels, Stories)
- **4:3** - Traditional television
- **21:9** - Ultra-wide cinematic (theatrical experience)

---

## Differences from the Gemini Format

| Feature     | Nano Banner                                      | Gemini/Midjourney          |
| ----------- | ------------------------------------------------ | -------------------------- |
| Structure   | Visual Description + Lighting & Mood separated   | Single prompt block        |
| Length      | 80-120 words + 30-50 words                       | 80-150 words total         |
| Format      | Episode Visual Script                            | Narrative descriptive      |
| Output      | Complete 3x3 grid in one pass                    | Generated one at a time    |
| Consistency | System guarantees consistency within a batch     | Seeds must be managed manually |
| Editability | Limited                                          | Adjustable one at a time   |

---

## Usage Recommendations

### Choosing a Platform

- **Prioritizing consistency** → Nano Banner
- **Need fine-grained control** → Midjourney v6
- **Rapid prototyping** → Gemini Imagen 3

### Choosing a Style

1. Choose the base style according to the story genre
2. Consider target audience preferences
3. Keep the style consistent across the whole series

### Choosing Lighting

1. Choose the dominant lighting according to the emotional tone of the plot
2. Switch lighting schemes at key plot turns
3. Keep lighting continuous within the same scene
