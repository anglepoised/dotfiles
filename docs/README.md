# dotfiles

My dotfiles, managed with [chezmoi](https://www.chezmoi.io/).

## Notes

### Dump homebrew

```sh
brew-bundle-dump
```

### Git secret scanning

This repo configures a global `pre-commit` hook (via `core.hooksPath`) that
uses `gitleaks` to block secrets from being committed.

### Repo-local commit-msg hook

This repo has a Conventional Commits check in `.githooks/commit-msg`.

No repo-local `core.hooksPath` override is needed. Global hooks live in
`~/.config/git/hooks`, and the global `commit-msg` hook dispatches to
`./.githooks/commit-msg` when present.
