# links

This action can be used in the following manner:

```yaml
jobs:
  links:
    runs-on: ubuntu-latest
    timeout-minutes: 2
    steps:
      - uses: HRC-PhD/.github/actions/links@vx
        with:
          github-token: ${{ secrets.GITHUB_TOKEN }}
```

where `x` is the `major` version of the action. If custom link checking is
required, one can add custom inputs through `lychee-args`, i.e.:

```yaml
jobs:
  linting:
    runs-on: ubuntu-latest
    steps:
      - uses: HRC-PhD/.github/actions/linting@vx
        with:
          github-token: ${{ secrets.GITHUB_TOKEN }}
          lychee-args:
            --base . --verbose --no-progress './**/*.md' './**/*.html'
            './**/*.rst'
```
