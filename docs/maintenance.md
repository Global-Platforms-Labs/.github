# Public-profile maintenance

| Step | Action | Completion check |
|---|---|---|
| Establish scope | Read the current profile, root README and asset references | The intended change names a concrete file and visible result |
| Edit | Use a branch and preserve the existing identity unless a redesign is requested | Diff contains only the intended text or asset change |
| Review | Check wording, links, alternative text and publication audience | No internal project or connection details are introduced |
| Preview | Inspect Markdown and images at the expected width | Text is readable and images load |
| Submit | Create a pull request with the result and validation | Reviewer can assess the exact diff |
| Merge | Follow repository checks and merge authorization | Merge commit is present on `main` |
| Verify | Read the saved files and inspect any changed profile rendering | Source and visible result agree |

- An editing agent follows the same file and review workflow as a human.
- Give it the intended text change, allowed files and expected appearance.
- It should inspect the actual source, explain any uncertainty and report its checks.
- For this small static repository, a bounded task and PR are normally sufficient; add a durable plan only when the change needs multiple dependent stages.
- Do not place credentials or internal operational instructions in this public repository.

Example task:

```text
Update the public navigation label in profile/README.md.
Preserve the existing destination URL, banner and affiliation.
Check the changed link and Markdown rendering, then report the diff.
```

- Repository structure: [overview](overview.md).
- Complete inventory: [profile module](modules/profile.md).
- Publication behavior: [feature guide](features/publication.md).
