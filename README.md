# GitHub Actions Linter

## INSTRUCTIONS for Super-Linter
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

