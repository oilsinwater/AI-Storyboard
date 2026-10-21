# Framework Map: Repo Method to Vault Screenwriting Sources

Scope: the practical screenwriting, character, and worldbuilding material in `2 Wiki/Concepts/`, `2 Wiki/Sources/`, and `1 Raw/ingested/` (Eric Edson's screenplay notes, K.M. Weiland's character-arc series, Dwight Swain, Ian Irvine, Orson Scott Card, Karl Iglesias, Brandon Sanderson, Tyler Edlin and Sergio Toppi on visual character design). The Holographic/Ternary framework is not adopted; see §7.

Headline: the repo's three-act, nine-beat method already matches the vault's practical sources. The sources sharpen the beat labels, add a character spine (Lie, Want, Need, Ghost), add scene rules (every scene turns), add a worldbuilding rule set (Sanderson's laws), and replace "even spacing" with percentage anchors. Status column: **Direct** = same idea, rename only; **Richer** = same idea, source adds a rule; **Gap** = repo has nothing; **Disagrees** = source contradicts the repo.

## 1. Story structure (scriptwriter-skill)

| Repo concept | Vault term | Source | Status |
|---|---|---|---|
| Three-act structure, 25/50/25 | Three acts. Weiland anchors: First Plot Point 20-25%, Midpoint 50%, Third Plot Point 75%, Climax from ~90%, Resolution last ~2%. Core Question: Ask / Acceptance / Answer, 25/50/25 | `character-development/Creating Stunning Character Arcs` Pt 8-15; `the-core-question.md` | Direct, now with anchors |
| Setup / Confrontation / Resolution | Act I: Normal World + Hook; Act II: "Acceptance", active persistence, not passive suffering; Act III: Climax + Resolution | Edson "Establish the Normal World"; `the-core-question.md` | Direct |
| Protagonist | Protagonist with the **Active Hero formula**: inciting incident pushes them into a dilemma; the choice in that dilemma defines the external goal; every obstacle links back to that choice | Edson, `screenplay-writing-notes.md` §Main character must want something | Richer |
| (none) | **Character spine**: the Lie the character believes, the Thing they Want, the Thing they Need, the Ghost (prior wound). Irvine/Card version: Prior Wound, Inner Need, Outer Goal, Stakes, Emotional Dilemma | Weiland Pt 2-4; `character-construction-framework.md` | Gap |
| (none) | **Want vs. Need**: the story ends when the want converges with the need; getting the want alone is tragedy | Edson §Level of Conflict | Gap |
| (none) | **Logline formula**: When [inciting incident] happens, [protagonist] decides to [action] against [antagonist] | Edson §Log line Formula | Gap (planning aid, not output) |
| (none) | **4-Goal Rule**: the external goal is Win, Stop, Escape, or Retrieve. A visible physical finish line forces a physical, filmable climax | Edson §The 4 Goal Rule | Gap. High value for a storyboard pipeline |
| (none) | **MICE quotient**: Milieu, Idea, Character, Event decides where the story must start and end; do not open in one and close in another | `mice-quotient.md` | Gap |
| (none) | **Dramatic question**: pose it between 1/6 and 1/3 in; raise, delay, answer; each answer opens the next | Edson §BMOC tools; `suspense-tools.md` | Gap |
| Conflict (implicit) | **Three layers**: Global (vs. world), Local (vs. people close), Inner (vs. self). Conflict is not contrast: opposing views are only drama once they collide over a shared goal | `dramatic-conflict-taxonomy.md`; `dramatic-situation.md` | Gap |
| Antagonist (unspecified) | Antagonist has a reason, traits opposite the protagonist, and must look insurmountable; reacts to each protagonist move by making things worse | `Craft Dynamic Antagonists`; Edson §Where is the Adversary; Irvine escalation | Gap |
| World-building consistency (rules obeyed, extend not contradict) | **Sanderson's laws**: 1) magic may solve problems only as far as the audience understands it; 2) limitations beat powers; 3) expand what exists before adding. Plus: a transformation must cost, reveal, and be irreversible | `hard-vs-soft-magic-sanderson.md`; `transformation-as-narrative-event.md`; `power-scaling-creep.md` | Richer |
| (none) | **Seminal image**: start from one striking image and build the world that makes it inevitable; too many seminal images means none is | `seminal-image.md` | Gap |
| Series continuity | Same; add Irvine's rule that stakes must still escalate across episodes, and the power-creep warning | `power-scaling-creep.md` | Direct |

## 2. Nine-beat distribution (GUIDELINES.md)

Beat count and three-act split stay. Labels come from Weiland and Edson. Two repo beats change meaning: "Opening" becomes a Characteristic Moment (the protagonist shown acting, with a turn), and "Initial Reaction" becomes the First Plot Point (a decision; Edson: a lead to whom things merely happen is boring).

| Beat | Act | Vault name | Anchor | Former repo label |
|---|---|---|---|---|
| 1 | I | Hook / Characteristic Moment in the Normal World | 0-10% | Opening |
| 2 | I | Inciting Event (involves the protagonist, moves the story, before Act II) | ~12% | Inciting Incident |
| 3 | I | First Plot Point: the choice that sets the external goal (Win/Stop/Escape/Retrieve) and poses the dramatic question | 20-25% | Initial Reaction |
| 4 | II | First Attempt: tools gained, closer to the Want, farther from the Need | 25-37% | First Attempt |
| 5 | II | First Pinch Point: antagonist pressure; things get worse | ~37% | Rising Complication |
| 6 | II | Midpoint: moment of truth; protagonist shifts from reaction to action; often a false victory | 50% | Midpoint Turn |
| 7 | II/III | Third Plot Point: low point; the old self dies; ultimate choice between Want and Need | ~75% | Low Point |
| 8 | III | Climax: the Lie is rejected; obligatory scene at the physical finish line | ~90% | Climax |
| 9 | III | Resolution: the New Normal; thematic question answered; next dramatic question opened | 98-100% | New Equilibrium |

Flags:
- **Act boundary of beat 7.** Weiland places the Third Plot Point at the start of Act III (75%); the repo keeps the Low Point in Act II. Both are defensible. Step 2 will label it "Act II/III turn" and keep the repo's 3/4/2 count so nothing downstream moves.
- **Beat 1 must still turn.** Weiland's Characteristic Moment and Edson's Normal World agree with the repo: open on the ordinary world, but show the protagonist doing something with a visible emotional shift. A static establishing beat fails the scene check in §3.
- **Percentages replace "even spacing."** See §4.
- **Snowflake Three-Disaster variant** (`snowflake-method.md`): disasters at beats 3, 6, 7 keep the middle from sagging. Compatible; noted, not adopted as a separate rule.

## 3. Scene-format rules (GUIDELINES.md, episode template)

| Repo rule | Vault term | Source | Status |
|---|---|---|---|
| `## Scene X - INT./EXT. Location - Time` | Friedman layer 1: time and setting ground the reader | `7 Essential Elements of Scene` | Direct, keep |
| Scene = description + action + dialogue | **Scene/Sequel**: Scene = Goal, Conflict, Disaster; Sequel = Reaction, Dilemma, Decision. A scene without a disaster ending is an "incident", not a scene. Shorter sequels = faster pace | `scene-sequel-format.md`; `scene-and-sequel-swain.md` | Gap |
| (none) | **Four Emotions check**: a character enters in one of mad / glad / sad / scared and leaves in another | `four-emotions-cinema.md`; Edson | Gap |
| (none) | **Mamet check**: Who wants what? What happens if they do not get it? Why now? | `scene-dynamics.md` | Gap |
| (none) | **Edson scene procedure**: name the protagonist's wound, fear, visible goal, and structural position; state the scene want; if the scene does not move toward or block the goal, cut it; write on-the-nose dialogue first, then rewrite as subtext | Edson §Making a Scene Better | Gap |
| (none) | **Public vs. private objective**: every scene is a power grab; each character has a public objective and a hidden one. This is where subtext comes from | Edson §Secrecy & Deception | Gap |
| Visual first; present tense; specific not general | Same; Friedman layer 2 (moment-by-moment action); Weiland "show, don't direct" | `7 Essential Elements`; Weiland | Direct |
| Scene-establishing description, 2-3 sentences | Same; worse-off endings create suspense, good news does not | Friedman layers 3 and 6 | Richer |
| Character first appearance: name, age, key features | **Body-first design**: silhouette, mass distribution, posture, and shape language (angular = strength, round = gentleness) carry story before costume; story can override function (the reluctant blacksmith is lanky). **Full detail first, then simplify** on later appearances | `character-design-visual.md`; `The Biggest Mistake with Character Design` | Richer; confirms the canonical/repeat rule |
| Dialogue: voice, no filler, subtext | **R = C + S / E**: a line is the Stimulus passed through the Character's background and motive toward the scene's Ending; flat dialogue skips C | `epic-writing.md` | Richer |
| Key Beat Candidates | Same; use the Weiland anchors in §2 to place them | | Direct |

## 4. Beat-selection criteria (storyboard-artist.md, playbook, review checklist)

| Repo criterion | Vault term | Source | Status |
|---|---|---|---|
| Turning point: something changes | The scene **turn**: emotional state differs at exit; a unit with no turn is an incident, not a beat | `scene-dynamics.md`; Swain | Direct |
| Story-essential: removing leaves a gap | Story-map rule: if you cannot say what purpose a stop serves, it is dispensable. **Prefer "transfer stations"**: moments where two plot threads (A story, B story) intersect | `subway-story-mapping.md`; `story-map-technique.md` | Richer |
| Emotionally significant | **Emotions of Structure** (curiosity, anticipation, surprise) and **Emotions of Theme** (sympathy, identification, empathy, transportation). A nine-beat set should carry both kinds | `emotions-of-structure.md`; `emotions-of-theme.md` | Richer |
| Visually distinct: one compelling image | **Seminal image**; the 4-Goal Rule guarantees a physical goal; Edson: show the climax setting before the climax | `seminal-image.md`; Edson §BMOC tools | Richer |
| Covers beginning / development / ending (1-3, 4-6, 7-9) | The nine anchors in §2 | Weiland | Direct |
| Evenly distributed across the timeline | **Disagrees.** Distribution follows the structural anchors (12 / 25 / 37 / 50 / 75 / 90 / 98%), not equal page gaps | Weiland | Disagrees |
| Each beat stands alone | Keep for image generation. Add **promise and payoff**: a planted hazard should appear in a later beat; the beat board as a whole must keep its promises | `suspense-tools.md` Promise Rule; `21-fast-hacks-suspense.md` | Richer |
| No mundane moments | Setbacks and failure create suspense; success and good news do not. Every scene is a power grab | Friedman; Edson | Direct |
| Fields Scene / Description / Purpose | Same. Purpose should name the structural job (which anchor) and the emotion it carries | | Direct |
| 9-grid → 4-panel refinement | **BMOC is fractal** (Beginning, Middle, Obstacle, Climax exists in every sequence). Dramatica's TIME modality gives the 4-panel pulse: Setup, Revelation, Conflict, Aftermath. Toppi's sequential three-beat is Preparation, Action, Reaction | `screenplay-structure-bmoc.md`; `dramatica-modalities.md`; `character-design-visual.md` | Richer: a 4-panel sequence has a named pulse |
| Choose 1-2 beats to expand | Expand the Midpoint or the Climax (highest suspense sits at the climax, not before it) | `suspense-tools.md` | Richer |
| (none) | **Three characters per panel maximum**; the trio is the minimum viable social structure for drama and the most a single composition holds | `narrative-trio.md`; `genre-graphic-novels.md` | Gap. Direct storyboard rule |

## 5. Character and cast tools (optional references for the scriptwriter)

- **Cast from plot** (`phillips-character-development-method.md`): list the usual, unusual, and outlandish cast for the same thumbnail; pick the one that makes the best story.
- **Narrative trio** (`narrative-trio.md`, `shonen-trio-formula.md`): protagonist / rival / mediator as a default episodic cast.
- **Modern archetypes** (`modern-pathetic-archetypes.md`, `21st-century-archetypes.md`): define characters by the systemic pressure they buckle under, not by medieval roles.
- **Genre pages** (`genre-thriller.md`, `genre-mystery.md`, `genre-horror.md`, `genre-drama.md`, `genre-science-fiction.md`, `genre-fantasy.md`): per-genre structural patterns and failure modes; SF and fantasy must establish world rules in Act I before stressing them.
- **Archetype-native families** (`archetype-native-story-framework.md`): a diagnostic only. If the plot feels false, check whether a conquest structure was imposed on a Caregiver or Creator protagonist. Not adopted as structure.

## 6. No equivalent, kept as production rules

4C framework, word counts, 180-degree rule, jump-cut rules, platform formats, motion prompts, output purity. The vault has no video-prompt material.

## 7. Not adopted

- **Holographic / Ternary framework** (`4 Agent/Templates/Holographic-Story/`): too abstract for a production skill; kept agnostic. Its scene card maps onto Swain's Scene/Sequel, which is what step 2 uses instead.
- **Save the Cat 15 beats** (`blake-snyder-beat-sheet.md`): the vault flags it as formulaic; the Weiland anchors cover the same ground with fewer beats.
- **Dramatica 8 characters, Polti's 36 situations, Booker's 7 plots**: taxonomies, not procedures; reference only.
