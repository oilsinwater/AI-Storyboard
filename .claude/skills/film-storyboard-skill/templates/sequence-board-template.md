# Sequence Board Output Format (Reference)

**This template shows the structure of a 4-panel sequence board**

**❌ Strictly prohibited in output**:

- Frontmatter metadata
- Template instructions
- "Next step" directives
- Any non-content notes

**✅ Output only**: The actual sequence board content

---

## Final Output Format

```markdown
# Sequence Board - Episode {XX}

## Sequence A: [From Beat X]

### Panel 1

[Shot type]. [Detailed visual description, inheriting character/scene/lighting and color from the beat board]

### Panel 2

[Shot type]. [Continuous action description]

### Panel 3

[Shot type]. [Continuous action description]

### Panel 4

[Shot type]. [Continuous action description]

## Sequence B: [From Beat Y]

### Panel 1

...

### Panel 2

...

### Panel 3

...

### Panel 4

...
```

## Key Requirements

- **Inheritance consistency**: Must inherit the character description, scene setting, and lighting/color scheme of the corresponding beat board
- **Action continuity**: Action is continuous across the 4 panels, with no gaps in the action
- **Screen direction**: Maintain the 180-degree rule
- **Smooth transitions**: Cuts between panels feel natural

## Agent Notes

- No frontmatter metadata
- No template instructions
- Exactly 4 panels per sequence
- Must be based on the approved beat board
- Write prompts as narrative English (for AI compatibility)
