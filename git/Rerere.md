# Git tools - Rerere

[`rerere`](https://git-scm.com/book/en/v2/Git-Tools-Rerere) is a tool to "reuse recorded resolution" of a merge conflict

This tool is useful to save the state of a merge resolution and then use it multiple times in multiple conflicts (e.g., when doing a big rebase).

How rerere works is caching the merge resolutions.
Then, when a merge conflict is detected in git, it will fallback to rerere and check if there is any exact recorded resolution.

To activate rerere tool, you can config the seeting in global git:
```
git config --global rerere.enabled true
```

