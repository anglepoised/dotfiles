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
