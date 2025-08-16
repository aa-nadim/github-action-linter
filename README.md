# Github Actions Linter

## References

- [Super-Linter GitHub Repo](https://github.com/super-linter/super-linter)
- [FreeCodeCamp Article](https://www.freecodecamp.org/news/github-super-linter/)

```yaml
---
name: Super-Linter
on: push
jobs:
  super-lint:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v4
      - name: Run Super-Linter
        uses: github/super-linter@v5
        env:
          DEFAULT_BRANCH: main
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
