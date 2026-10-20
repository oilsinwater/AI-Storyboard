# Beat Board Output Format (Reference)

**This template shows the correct nano banner output structure**

**❌ Strictly prohibited in output**:

- Frontmatter metadata (`---\nepisode: ep01\n---`)
- Template instructions, notes
- "Next step" or workflow directives
- Any non-prompt content

**✅ Output only**: The actual beat board content (see format below)

---

## Nano Banner Format (Default - Recommended):

```markdown
EPISODE {XX}: BEAT BOARD VISUAL SCRIPT

Visual Description: [Detailed visual description: shot type, character/subject, action, scene, key visual elements - 80-120 words]
Lighting & Mood: [Light direction, quality, color temperature, and emotional atmosphere - 30-50 words]

Beat 2: [Beat title]
Visual Description: ...
Lighting & Mood: ...

Beat 3: [Beat title]
Visual Description: ...
Lighting & Mood: ...

Beat 4: [Beat title]
Visual Description: ...
Lighting & Mood: ...

Beat 5: [Beat title]
Visual Description: ...
Lighting & Mood: ...

Beat 6: [Beat title]
Visual Description: ...
Lighting & Mood: ...

Beat 7: [Beat title]
Visual Description: ...
Lighting & Mood: ...

Beat 8: [Beat title]
Visual Description: ...
Lighting & Mood: ...

Beat 9: [Beat title]
Visual Description: ...
Lighting & Mood: ...
```

## Why This Format Suits Nano Banner:

1. **Clear structure** - Each beat is explicitly labeled
2. **Separation of concerns** - Visual description is independent of lighting/mood
3. **Consistent format** - Easy for nano banner to parse
4. **Narrative flow** - Reads like a visual script
5. **Character consistency** - The canonical description is repeated across all beats

## Midjourney v6 Format:

```markdown
## Beat 1: [Title] (Top-Left)

[Detailed prompt] --ar 16:9 --style cinematic --v 6

## Beat 2: [Title] (Top-Center)

...
```

## Gemini/DALL-E Format:

Individual beat prompts, no special format requirements.

## Agent Notes:

- **No frontmatter metadata**
- **No template instructions**
- **Use a consistent canonical character description**
- **Visual Description should be detailed** (80-120 words)
- **Lighting & Mood should be specific** (30-50 words)
- **Narrative English prompts** (AI compatibility)
