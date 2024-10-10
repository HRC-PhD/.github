# Default pre-commit config

In a repository that requires [pre-commit](https://pre-commit.com), simply add a
file called `.pre-commit-config.yaml` with the following code.

```yaml
repos:
  - repo: https://github.com/HRC-PhD/.github
    rev: v0.1.0
    hooks:
      - id: hrc-phd-hooks
```

Then run `pre-commit install; pre-commit autoupdate`.
