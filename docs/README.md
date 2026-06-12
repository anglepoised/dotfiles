# dotfiles

My dotfiles, managed with [chezmoi](https://www.chezmoi.io/).

## Notes

### Dump homebrew

```sh
brew-bundle-dump
```

### Git secret scanning

This repo configures a global `pre-commit` hook (via Git hook config) that
uses `gitleaks` to block secrets from being committed.

### Repo-local commit-msg hook

This repo has a Conventional Commits check in `.githooks/commit-msg`.

No repo-local `core.hooksPath` override is needed. The global `commit-msg`
hook config dispatches to `./.githooks/commit-msg` when present.
