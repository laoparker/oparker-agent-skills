---
name: skill-trigger-test
description: Test whether an agent skill actually triggers. Use when a skill was just written, when a skill does not trigger, or when the user asks to test a skill with different phrasings.
---

# Skill Trigger Test

1. Write the expected phrasing the user would naturally use.
2. Write a second phrasing with the same meaning but different words.
3. Run both. Both must trigger the skill.
4. If either fails, fix the description first, not the body.
5. Add the missing user phrasing to the description, then test again.
