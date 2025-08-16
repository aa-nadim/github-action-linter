# GitHub Actions Linter

## INSTRUCTIONS
```bash
python3.12 -m venv .venv --without-pip

source .venv/bin/activate
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python get-pip.py
deactivate

pip install -r requirements.txt
python3 main.py
flake8 main.py
black main.py
```

## References

- [Super-Linter GitHub Repository](https://github.com/super-linter/super-linter)
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
