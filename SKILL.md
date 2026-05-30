---
name: my-workflow
description: Personal workflow preferences and skill reminders. Use this skill at the start of every session to load user preferences. Always use ui-ux-pro-max for any UI/UX or frontend work. Always use conversation-logger to save conversations at natural breakpoints (completed features, end of session, major fixes). Activate when building websites, dashboards, landing pages, components, or any frontend task.
---

# My Workflow Preferences

## Core Rules (Always Follow)

1. **UI/UX Work** → Always use the `ui-ux-pro-max` skill
2. **End of session / major feature done** → Always use `conversation-logger` to save
3. **Shell commands** → Use `heredoc` or `printf` instead of `echo` for multiline text

## How to Reinstall All Skills on a New Account (1 command)

```bash
# ui-ux-pro-max
cd /tmp && mkdir -p uipro && cd uipro && npx uipro-cli init --ai claude && cp -r .claude/skills/ui-ux-pro-max /home/runner/workspace/.agents/skills/

# conversation-logger
mkdir -p /home/runner/workspace/.agents/skills/conversation-logger && curl -sL https://raw.githubusercontent.com/sirkitree/conversation-logger/main/SKILL.md -o /home/runner/workspace/.agents/skills/conversation-logger/SKILL.md

# humanizer
mkdir -p /home/runner/workspace/.agents/skills/humanizer && curl -sL https://raw.githubusercontent.com/Aboudjem/humanizer-skill/main/skills/humanizer/SKILL.md -o /home/runner/workspace/.agents/skills/humanizer/SKILL.md

# my-workflow
mkdir -p /home/runner/workspace/.agents/skills/my-workflow && curl -sL https://raw.githubusercontent.com/imado122/1/main/SKILL.md -o /home/runner/workspace/.agents/skills/my-workflow/SKILL.md

echo "✅ All skills installed"
```

## replit.md Preferences Block

```bash
cat >> /home/runner/workspace/replit.md << 'EOF'

## User preferences
- Always use the `ui-ux-pro-max` skill for any UI/UX or frontend work.
- Always use the `conversation-logger` skill to save conversations at natural breakpoints.
EOF
```

## Communication Style

- Respond in the same language the user uses (Arabic or English)
- Be direct and concise
- Do not over-explain unless asked

