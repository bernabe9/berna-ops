# Skills

Skill definitions that instruct the agent how to perform specific tasks.

## Purpose

Skills provide specialized knowledge and workflows. When activated, the agent
follows the skill's instructions to complete tasks consistently.

## Creating a Skill

1. Create a folder with the skill name (lowercase, hyphens):
   ```
   skills/my-skill/
   ```

2. Create `SKILL.md` with YAML frontmatter:
   ```markdown
   ---
   name: my-skill
   description: This skill should be used when the user asks to "do X",
     "perform Y", or requests Z.
   ---

   # My Skill

   ## Purpose
   What this skill accomplishes.

   ## Process
   Step-by-step instructions...
   ```

## Skill Structure

```
skills/
└── skill-name/
    ├── SKILL.md        # Required - instructions
    ├── LEARNINGS.md    # Auto-created - accumulated insights
    ├── scripts/        # Optional - Python scripts
    ├── references/     # Optional - detailed docs
    └── assets/         # Optional - templates, data
```

## Naming Rules

- 1-64 characters
- Lowercase letters, numbers, hyphens only
- Cannot start/end with hyphen
- No consecutive hyphens
- Must match folder name

## Description Format

Use third-person trigger phrases:
```yaml
description: This skill should be used when the user asks to "review code",
  "check quality", or requests feedback on changes.
```

## Example Skills

- `code-review` - Code quality analysis
- `job-description` - Writing job postings
- `documentation` - Creating technical docs
- `data-analysis` - Analyzing datasets
