# Translation Audit (2026-10-20)

Four parallel reviews of every agent, skill, template, and README file for residual Chinese-to-English translation errors. No CJK characters, fullwidth punctuation, or escaped `\*\*` remain anywhere. What remains is calques, wrong technical terms, stale counts, and a few logic mismatches.

Plan column: **apply** = fix as proposed; **apply (alt)** = fix with the alternative noted; **skip** = leave, reason given; **ask** = needs a decision.

## Repo-wide decisions

| Topic | Occurrences | Recommendation | Plan |
|---|---|---|---|
| "9-grid" (calque of 九宫格) | CLAUDE.md commands, README, all agents, templates, checklist; playbook says "9-panel" | Keep "9-grid" as the product term for the beat board (it is a 3x3 grid of 9 and is used in user-facing commands). Change the playbook's "9-panel" to "9-grid" for consistency. Change "source 9-grid" to "source beat board" where it means the artifact | ask |
| "axis" / "axis stability" / "axis rules" (calque of 轴线) | README 48, 170, 337, 565; sequence-board-template 62 | Replace with "180-degree rule" / "screen direction" | apply |
| "4C Framework" lists Clear, Concise, Consistent, Progressive (three C's) | film-storyboard SKILL.md 21-26, README, director.md | Keep the "4C" name (referenced everywhere); no rename | skip |
| Headings ending in ":" | beat-board, beat-breakdown, sequence-board templates | Drop trailing colons | apply |
| "Narrative English prompts (AI compatibility)" | beat-board-template 89, sequence-board-template 71 | "Write prompts as narrative English (for AI compatibility)" | apply |
| "sequel" meaning "next episode" clashes with Swain's Scene/Sequel (introduced in step 2) | scriptwriter SKILL.md 11; GUIDELINES 352, 443 | "continuing episode" / "a question for the next episode" | apply |
| Anchor list with 8 items (introduced in step 2) | scriptwriter.md 18, 161; scriptwriter SKILL.md 119; GUIDELINES 440 | Add "First Attempt", say "First Pinch Point" | apply |
| Leftover "this document is written in English because..." notes | playbook 10; motion-prompt-methodology 10; gemini guide 16 | Delete | apply |
| Uppercase sluglines (INT. SUBWAY CAR - NIGHT) | scriptwriter SKILL.md 158, GUIDELINES 22, episode template | Project convention is mixed case; leave | skip |
| README line counts and "607 lines (optimized -39.4%)" stats | README 407, 421, 608 | Remove the numbers rather than maintain them | apply (alt) |

## Agents and README

| File | Line | Current | Proposed | Sev | Plan |
|---|---|---|---|---|---|
| .claude/CLAUDE.md | 16 | sequence board (4-frame) | sequence board (4-panel) | error | apply |
| .claude/CLAUDE.md | 52 | **Skill Expansion** | **Skill Structure** | awkward | apply |
| animator.md | 17 | **Timing Planning** | **Timing** | awkward | apply |
| animator.md | 105 | Handheld: Handheld camera shake | Handheld: slight organic camera shake | awkward | apply |
| director.md | 52, 88, 100 | 9-Grid / source 9-grid | see repo-wide | awkward | ask |
| director.md | 92 | Actions and behavior flow logically between panels | Action flows logically from panel to panel | awkward | apply |
| director.md | 114 | one primary action/behavior | one primary action | awkward | apply |
| director.md | 184 | Safety issues | Edit-safety issues | awkward | apply |
| scriptwriter.md | 3, 11 | beat breakdown and shot design | beat breakdown and shot planning | awkward | apply |
| scriptwriter.md | 18, 161 | 8-item anchor list | 9 anchors | error | apply |
| scriptwriter.md | 101 | Give the antagonist a reason | Give the antagonist a motive | awkward | apply |
| storyboard-artist.md | 33 | Each turn: ... | Each turns: ... | awkward | apply |
| storyboard-artist.md | 37 | Each convey the story on their own | Each conveys its story moment on its own | error | apply |
| storyboard-artist.md | 129 | too long (>150 words) or too short (<80 words) | >170 words / <110 words total | error | apply |
| README.md | 3 | ...used to automate the film storyboarding workflow | ...that automates the film storyboarding workflow | awkward | apply |
| README.md | 47, 169 | Continuous 4-shot sequence | 4-panel sequence | awkward | apply |
| README.md | 48, 170, 337, 565 | axis stability / axis rules / axis violations | 180-degree rule / screen direction | awkward | apply |
| README.md | 138 | Scriptwriter reads script/ep01-awakening.md | Storyboard Artist reads ... | error | apply |
| README.md | 242 | Layered Progressive Process | Progressive Refinement | awkward | apply |
| README.md | 292, 361 | conceive a story / Conceive new stories | develop a story / Develop new stories | awkward | apply |
| README.md | 352 | Schedule the workflow | Drive the workflow | awkward | apply |
| README.md | 384 | Read-only, does not create | Read-only; does not create artifacts | awkward | apply |
| README.md | 407, 421 | SKILL.md (139 lines) / (165 lines) | drop line counts | awkward | apply (alt) |
| README.md | 411 | 6 candidate lighting schemes | 6 lighting scheme options | awkward | apply |
| README.md | 520 | Sequence 1 (based on Beat 1-2) | (based on Beat 1) | awkward | apply |
| README.md | 524 | move quickly past in opposite direction | ...in the opposite direction | error | apply |
| README.md | 532 | Describe with visualizable action, avoid abstract... | Describe through visible action; avoid abstract psychology | awkward | apply |
| README.md | 539 | Fix character appearance in Beat 1 | Lock character appearance in Beat 1 | awkward | apply |
| README.md | 560 | all beats use the same keywords | ...the same identifiers | awkward | apply |
| README.md | 608 | 607 lines (optimized -39.4%) | drop the stat | awkward | apply (alt) |

## film-storyboard-skill

| File | Line | Current | Proposed | Sev | Plan |
|---|---|---|---|---|---|
| SKILL.md | 18, 26, 122 | 9-Grid / 9-grid | see repo-wide | awkward | ask |
| SKILL.md | 21-26 | 4C Framework | keep | awkward | skip |
| SKILL.md | 37-41 | fields "Core action", "Emotional value" | Title, Scene reference, Description, Purpose (match template) | error | apply |
| SKILL.md | 40-41 | "Use template:" indented into list | own paragraph | awkward | apply |
| SKILL.md | 64 | with the pulse Setup → ... | following the arc Setup → ... | awkward | apply |
| SKILL.md | 108 | 6 candidate lighting schemes | 6 lighting scheme options | awkward | apply |
| REFERENCE.md | 15 | Generates the complete 9-grid in a single pass | Generates all 9 panels in a single pass | awkward | apply |
| REFERENCE.md | 39 | Grid position labeled | Label each beat's grid position | awkward | apply |
| REFERENCE.md | 121 | Candidate Lighting Schemes | Lighting Scheme Options | awkward | apply |
| REFERENCE.md | 183 | Differences from the Gemini Format | Nano Banana vs Gemini/Midjourney Formats | awkward | apply |
| gemini guide | 4 | refer to it only when confused or when needed | refer to it only when unsure | awkward | apply |
| gemini guide | 16 | Prompt content is written in English for the best... | Write prompts in English | awkward | apply |
| gemini guide | 263 | Hair-raising, momentous atmosphere | Charged, momentous atmosphere | awkward | apply |
| gemini guide | 326, 329 | "(65 words)" / "Exceeds the 50-word limit" but sample is 50 words | lengthen sample so it genuinely exceeds, fix count | error | apply |
| playbook | 10 | "written in English because..." note | delete | error | apply |
| playbook | 12 | duplicate of line 8 | delete one | awkward | apply |
| playbook | 66 | "(62 words)" example is 38 words, below the stated minimum | replace with a valid 80-120 word example | error | apply |
| playbook | 172 | "the gaps around the climax are the shortest" contradicts the page example | reword to "the gaps at the end are short" | awkward | apply |
| playbook | 801 | from source 9-panel | from the source beat | awkward | apply |
| beat-board-template | 16, 58, 66, 78, 82 | headings end in ":" | drop colons | awkward | apply |
| beat-board-template | 89 | Narrative English prompts (AI compatibility) | reword | awkward | apply |
| beat-breakdown-template | 16, 42 | headings end in ":" | drop colons | awkward | apply |
| sequence-board-template | 16, 58, 65 | headings end in ":" | drop colons | awkward | apply |
| sequence-board-template | 61 | with no jumps | with no gaps in the action | awkward | apply |
| sequence-board-template | 62 | **Axis stability**: Obey the 180-degree rule | **Screen direction**: Maintain the 180-degree rule | error | apply |
| sequence-board-template | 63 | **Smooth shots**: Transitions between panels are natural | **Smooth transitions**: Cuts between panels feel natural | awkward | apply |
| sequence-board-template | 71 | Narrative English prompts (AI compatibility) | reword | awkward | apply |

## animator-skill and storyboard-review-skill

| File | Line | Current | Proposed | Sev | Plan |
|---|---|---|---|---|---|
| animator SKILL.md | 60 | Motion first (25 words), example is 20 | drop the count | awkward | apply (alt) |
| animator SKILL.md | 63 | across platform | across the platform | awkward | apply |
| animator SKILL.md | 142 / 205 | "40-80 word" vs "~25 words" fix line | say "40-80 words" | error | apply |
| animator SKILL.md | 181 | Director feedback on motion clarity issues | Director feedback flags motion clarity issues | awkward | apply |
| MOTION_LIBRARY | 32 | waves hand greeting | waves hand in greeting | awkward | apply |
| MOTION_LIBRARY | 58 | slow pan upward (under Pan) | slow tilt upward, move to Tilt | error | apply |
| MOTION_LIBRARY | 59 | camera pans down from sky to ground | camera tilts down | error | apply |
| MOTION_LIBRARY | 69 | to establish shot | to establishing shot | error | apply |
| MOTION_LIBRARY | 156 / 219 | Slow Motion / Fast Motion (means slo-mo) | Slow-Paced Motion / Fast-Paced Motion | awkward | apply |
| MOTION_LIBRARY | 173 | Aesthetic showcases | Beauty shots | awkward | apply |
| MOTION_LIBRARY | 205 | Real-life pacing | Naturalistic pacing | awkward | apply |
| MOTION_LIBRARY | 364 | dynamic showcases | dynamic action | awkward | apply |
| MOTION_LIBRARY | 385 | Turn head 180 degrees (plausibility section) | Turn head 90 degrees | error | apply |
| MOTION_LIBRARY | 388 | Change of expression into a smile | Expression changes to a smile | awkward | apply |
| MOTION_LIBRARY | 456 | **Refresh date**: (no date) | **Maintenance note**: | awkward | apply |
| methodology | 1 / 6 | two H1 headings | keep one | awkward | apply |
| methodology | 10 | "written in English because..." | delete | error | apply |
| methodology | 34, 45, 497 | stated word counts wrong | fix counts | awkward | apply |
| methodology | 49 / 57 | "Camera static, following her motion with a slow pan" | "Camera pans slowly to follow her" | error | apply |
| methodology | 509 | "Solution (52 words)" is 37 words, below the 40 floor | pad to 40+ and fix count | error | apply |
| methodology | 606 | 3-8 seconds typical vs 3-5 elsewhere | 3-5 seconds | awkward | apply |
| methodology | 1197-1198 | Medium 2-3 s / Fast 1-2 s vs library Medium 3-4 / Fast 2-3 | align to the library | error | apply |
| methodology | 1203 | Animator should internalize | The Animator should internalize | awkward | apply |
| methodology | 1204 | "onsistency with the storyboard..." orphan fragment | restore the sentence | error | apply |
| motion-prompt-template | 10 / 14 | Motion 2 (From Sequence B, Panel 1) | (From Sequence A, Panel 2) | error | apply |
| motion-prompt-template | 23 | [Shot specification] not in SKILL.md structure or example | drop it | awkward | apply |
| review-checklist | 145 | "it is shown (not jumped)" | "the crossing is shown on screen, not cut across" | awkward | apply |
| review-checklist | 187 | typically 3-5 seconds | keep (methodology aligns to it) | awkward | skip |
| review-checklist | 193 | Too short (<30 words) | <40 words | awkward | apply |
| review-checklist | 215 | Character runs left, camera pans right | camera pans left to follow | awkward | apply |
| review-checklist | 306 | Safety issues | Edit-safety issues | awkward | apply |
| review-checklist | 307 | 4-panel does not match the source 9-grid | 4-panel sequence does not match its source beat | awkward | apply |

## scriptwriter-skill

| File | Line | Current | Proposed | Sev | Plan |
|---|---|---|---|---|---|
| SKILL.md | 11 | series continuity and sequel creation | continuing a series from previous episodes | awkward | apply |
| SKILL.md | 119 | 8-item anchor list | 9 anchors | error | apply |
| SKILL.md / GUIDELINES | 163 / 27 | symbols ... are reflected on her face | The glow of dense handwritten symbols and a six-pointed star lights her face | awkward | apply |
| SKILL.md | 162 | notebook vs diary (template) | the sample scene and the template describe different episodes; leave | awkward | skip |
| SKILL.md / GUIDELINES | 158 / 22 | mixed-case slugline | project convention | awkward | skip |
| GUIDELINES | 36 | INT./EXT. = Contains both interior and exterior | the scene moves between interior and exterior (a car, a doorway) | awkward | apply |
| GUIDELINES | 41 | Relative time: same time, later, the next day | add "continuous" | awkward | apply |
| GUIDELINES | 75 | Name (if any) | Name (or a descriptor if unnamed, e.g. MYSTERIOUS FIGURE) | awkward | apply |
| GUIDELINES | 84 | LILY (teenage, around 16, | LILY (16, | awkward | apply |
| GUIDELINES | 105 vs 26, 258 | three different canonical Emma descriptions | unify: waist-length silver hair, violet eyes, dark red coat | awkward | apply |
| GUIDELINES | 150 | Her hand grabs the handle and shoves it open | She grabs the handle and shoves the door open | awkward | apply |
| GUIDELINES | 156 | wrong example does not show the mistake | "Emma ran to the door and it was opened." | awkward | apply |
| GUIDELINES | 222, 331 | burns her apartment | burns down her apartment | awkward | apply |
| GUIDELINES | 223, 332 | takes the offensive | goes on the offensive | awkward | apply |
| GUIDELINES | 253 | First Appearance vs Repeat Appearance | First Appearance vs Later Appearances | awkward | apply |
| GUIDELINES | 310 | "find the book's owner (Retrieve)" | align with "retrieve the diary" | awkward | apply |
| GUIDELINES | 342, 350 | Rallying | Regrouping | awkward | apply |
| GUIDELINES | 352 | a sequel question is planted | a question for the next episode is planted | error | apply |
| GUIDELINES | 383 | "Young man, this matter is far more complicated than you imagine. I suggest you think twice before acting." | "Young man, this is a good deal more complicated than you think. I'd think twice before doing anything." | awkward | apply |
| GUIDELINES | 443 | If a sequel, character appearance... | If a continuing episode, ... | error | apply |
| episode-template | 52 | Key Beat Candidates "optional" contradicts "must include ≥9" | state it is required | awkward | ask |
| episode-template | 57 | "3. **Beat 9**" | "9. **Beat 9**" | error | apply |
| episode-template | 81 | (murmuring to herself) | (to herself) | awkward | apply |
| episode-template | 88 | INT. Void Passage - Time Has No Meaning | INT. Void Passage - Continuous | awkward | apply |
| episode-template | 96 | "She begins to understand this is not a dream." (unfilmable); EMMA re-capitalized | "Her expression shifts from fear to focus." and lowercase Emma | awkward | apply |
| episode-template | 104-112 | beat list lacks anchor labels | add "(Scene 1, Hook)" etc. | awkward | apply |
