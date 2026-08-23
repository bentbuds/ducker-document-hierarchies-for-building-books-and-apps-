---
description: Handle PR comments and address feedback
---

Check comments on the current PR. Retrieve both top-level review bodies and inline review comments. Evaluate each comment on technical merit rather than automatically agreeing.

If feedback is reasonable, present a concrete fix plan first and wait for Ducker's approval before changing code.

When using GitHub CLI, remember that `gh pr view --json reviews` does not include inline comments. Also fetch:

```bash
gh api repos/{owner}/{repo}/pulls/{pr_number}/comments
```
