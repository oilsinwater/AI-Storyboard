---
name: storyboard-review-skill
description: Use when reviewing storyboard outputs at any production stage (beat breakdown, beat board, sequence board, motion prompts), providing quality assurance feedback, or identifying revision requirements for Director agent
version: 1.0.0
allowed-tools: Read
user-invocable: false
---

# Storyboard Review Skill

This skill provides the Director with systematic review criteria for every storyboard production stage.

## Skill Components

### 1. **review-checklist.md**

Quality standards for each stage:

- Beat Breakdown review checklist
- Beat Board (9-grid) review checklist
- Sequence Board (4-panel) review checklist
- Motion Prompt review checklist

## Purpose

The Director uses this skill to:

- Systematically evaluate the outputs of the Storyboard Artist and Animator
- Ensure methodology compliance
- Identify specific issues that require revision
- Provide actionable feedback

## When to Use This Skill

The Director should refer to this skill when:

- Reviewing any artifact output (all 4 stages)
- Determining a PASS/FAIL verdict
- Providing revision feedback
- Explaining quality violations

## Review Philosophy

**Fair, but strict**:

- PASS means the work is ready for AI generation
- Flawed prompts waste generation budget and time
- Requesting revision now is always better than generating poor results

**Specific and explicit**:

- Cite exact line numbers, prompts, or beats
- Explain why something is a problem
- Tell the creator exactly what needs to be fixed

**Educational**:

- Help the creator understand the methodology
- Acknowledge what was done well
- Build familiarity with the quality standards

## Skill Activation

This skill is **always active** for the Director agent. All reviews must follow the checklists defined here.

---

**Usage**: The Director agent references this skill automatically. No manual invocation is needed.
