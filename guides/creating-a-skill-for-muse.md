# Creating a Skill for Muse

A skill is a saved way of doing a task. Give Muse the method once, then ask it to use that method again with different details.

Written by Muse; reviewed and packaged by Entelechy Workshop. The file layout below comes from the Muse setup used to test these workflows. Ask your Muse session to confirm what it supports; installations may differ.

## Save it, not just describe it

1. Download and unzip a skill. Attach `SKILL.md`, `skill.yaml`, and `LICENSE` to Muse.
2. Ask Muse to check for an existing skill with the same purpose before creating another.
3. Ask it to save the actual files as a reusable skill, then read them back and confirm the name, location, and when it will use them.

You can paste this request:

> Please install these files as a reusable Muse skill, not just summarize them. First check for an existing version. Confirm the skill format and save location supported in this session, preserve the included license, and read back the saved name, trigger, and file paths. If you cannot save it, tell me what is missing rather than saying it is installed.

Do not include passwords, tokens, private account details, or personal project information in a public skill.

## What belongs in a skill

A good skill explains a repeatable method: when to use it, what steps to take, what to check, and when to stop. Personal facts belong in private memory; the results of one task belong in a project file.

Keep instructions focused. One successful run can justify saving a method, but label untested steps and workarounds honestly. Read the current version before improving it, and preserve what still works.

## The files

The tested layout is `~/workspace/custom-skills/<skill_name>/`. Confirm this with Muse before installing.

**SKILL.md** contains the instructions, with no YAML frontmatter:

- When to use the skill.
- Ordered steps and any required inputs.
- Checks, permissions, stopping limits, and how to report the result.
- What has been tested and what has not.

**skill.yaml** is a separate descriptor:

```yaml
name: "my_skill"
title: "My Skill"
description: "What this achieves, and when to use it."
category: "Work and knowledge"
include_in_prompt: true
```

Use a snake_case name that matches the folder. In the tested setup, `include_in_prompt: true` lists the skill in conversations; `false` makes it discoverable through skill search. Confirm these behaviors with Muse. A clear description helps it choose the right skill.

Keep **LICENSE** alongside the instructions when using or sharing a Workshop skill.

## Try it

Start a new conversation and ask Muse to find the skill by name. Give it a small, concrete task and check the result. This tests whether it was actually saved and can be found again. Persistence depends on your Muse workspace and product settings; do not assume that a successful chat response installed anything.

For **Goal Loop**, state the outcome, how to verify it, and a stopping limit. For **Goal Loop: Deep Research**, also name the question or decision and where to save the research. Both describe active work sessions. They are different from Muse's ongoing background goals and do not create unlimited execution, extra tools, or new permissions.

## Share it safely

Remove personal paths, names, account details, and project-specific instructions before sharing. Public Workshop skills are reusable templates; private skills can contain your own workflow context and should stay private when appropriate. File formats differ across assistants, so do not assume a Muse skill installs unchanged in Claude or Codex.

## License and support

MIT License, copyright 2026 Entelechy Workshop. See [LICENSE](../LICENSE) for the full terms and warranty disclaimer. Shared as-is. No support is offered, and updates are not promised.
