# CLAUDE.md

## GitHub Actions runners

- Never use `ubuntu-latest`; the `runner-labels` check fails on it (RD-2286).
- New workflows: `runs-on: ubuntu-26.04`.
- Changing an existing workflow: move all its jobs from `ubuntu-24.04` to `ubuntu-26.04` in the same PR and get CI green. Deploy/release workflows move only after the repo's CI is green on 26.04.
