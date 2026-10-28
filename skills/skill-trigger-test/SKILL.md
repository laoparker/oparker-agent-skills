---
name: skill-trigger-test
description: Test whether an agent skill actually triggers. Use when a skill was just written, when a skill does not trigger, or when the user asks to test a skill with different phrasings.
---

# Skill Trigger Test

Use this after you write or change a skill. A skill passes only if two different user phrasings both trigger it.

## Test in 2 minutes

1. Pick the skill to test.
2. Write phrasing A: the wording you expect the user to use.
3. Write phrasing B: the same meaning, different words, and do NOT reuse the skill's trigger words.
4. Run A and B in two fresh sessions. Both must trigger the skill.
5. If either fails, fix the description first, not the body. Add the missing user wording to the description, then test again.

Pass: A triggers, B triggers.
Fail: only A triggers. That usually means the description only matches your own wording, not the user's.

## Worked example

Skill to test: a commit-message skill.

- Phrasing A: "写个提交信息"
- Phrasing B: "这次改动怎么总结给同事看？"
- Expected: both trigger the commit-message skill.
- If B fails: the description is missing "总结改动" type wording. Add it to the description, for example:

Before: "Helps with git stuff."
After: "Write a conventional commit message. Use when the user asks to write a commit message, summarize changes, or explain what changed."

Then run A and B again.

## Copy checklist

- [ ] Phrasing A triggers
- [ ] Phrasing B triggers, without reusing trigger words
- [ ] If B fails, description was fixed first, not the body
- [ ] The missing wording from B is now in the description
- [ ] Both phrasings pass on retest
