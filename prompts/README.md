# Prompt Pack

Harness-independent system prompts for the storyboard pipeline. Each file stands alone: paste it as the system prompt of any chat model (local or hosted) and supply the inputs in the user turn. Nothing here depends on tools, file access, or an agent framework.

## Files

| File | Role | Input in the user turn | Output |
|---|---|---|---|
| `scriptwriter.txt` | Scriptwriter | premise, tone, length, style, previous episodes | `ep{XX}-{title}.md` |
| `storyboard-artist.txt` | Storyboard Artist (Stages 1-3) | the script, then the approved breakdown, then the approved beat board | `beat-breakdown-ep{XX}.md`, `beat-board-prompt-ep{XX}.md`, `sequence-board-prompt-ep{XX}.md` |
| `director.txt` | Director (quality gate) | one artifact plus its source (script, breakdown, or beat board) | a review ending in PASS or FAIL |
| `animator.txt` | Animator (Stage 4) | the approved sequence board | `motion-prompt-ep{XX}.md` |
| `templates/*.txt` | Output formats | attach to the user turn if the model drifts from the format | |

## Running the pipeline by hand

1. Scriptwriter: system prompt `scriptwriter.txt`; user turn gives the premise. Save the result as the script.
2. Storyboard Artist, Stage 1: system prompt `storyboard-artist.txt`; user turn says "Generate the beat breakdown" and pastes the script.
3. Director: system prompt `director.txt`; user turn pastes the breakdown and the script. On FAIL, send the numbered issues back to the Artist conversation and ask for a revision; re-review until PASS.
4. Storyboard Artist, Stage 2: "Generate the beat board, platform Nano Banana, style <style keywords>" with the approved breakdown and the script. Director reviews.
5. Storyboard Artist, Stage 3: "Generate the sequence board, expand Beats 6 and 8" with the approved beat board. Director reviews.
6. Animator: system prompt `animator.txt`; user turn pastes the approved sequence board. Director reviews.

Keep each role in its own conversation so the Director's feedback can be sent back to the same Artist context.

## Limits that every prompt enforces

- Nine beats at the structural anchors: Hook, Inciting Event, First Plot Point, First Attempt, First Pinch Point, Midpoint, Third Plot Point, Climax, Resolution.
- Beat board: Visual Description 80-120 words plus Lighting & Mood 30-50 words (110-170 total); single-block Gemini or Midjourney prompts 80-150 words.
- Sequence board: 4 panels per sequence, 80-150 words each, at most three characters per panel.
- Motion prompts: one per panel, 40-80 words, 3-5 seconds.
- Character descriptors repeated word for word across every prompt in which the character appears.

## Local model notes

Models under about 8B parameters tend to lose the word limits and the verbatim-descriptor rule. Ask the Director to count words explicitly (the prompt already does), and attach the matching template file to the Artist's user turn when the format drifts. The Director prompt is also usable as a self-check: paste an artifact into a fresh Director conversation before generating images.
