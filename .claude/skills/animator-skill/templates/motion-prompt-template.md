# Motion Prompt Output Format (Reference)

**This template shows the structure - the final output must not contain these instructions**

## The final output should contain:

```markdown
# Motion Prompts - Episode {XX}

## Motion 1 (From Sequence A, Panel 1)

[40-80 word action-oriented prompt describing motion, camera, pacing, duration]

## Motion 2 (From Sequence A, Panel 2)

[40-80 word prompt]

...
```

## Motion Prompt Structure:

[Subject] [primary action] [direction] [+ camera movement]. [Pacing]. [Duration: X seconds].

## Example:

```
A woman with silver hair in a crimson coat walks from left to right along a train platform,
wind blowing her hair. Camera pans right to follow her. Steady walking pace. 5 seconds.
```

## Agent Notes:

- No frontmatter metadata
- No template instructions
- Output only the actual motion prompts (40-80 words each)
- Focus on: motion, direction, speed, duration
- Simpler than image prompts - focus on action
