
## 2. CI Pipeline: Test Automation

### File: `.github/workflows/ci.yml`

```yaml
name: CI Pipeline

on:
  push:
    branches: ["*"]
  pull_request:
    branches: [main]

jobs:
  test:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v3

      - name: Set up Python
        uses: actions/setup-python@v4
        with:
          python-version: '3.10'

      - name: Install dependencies
        run: |
          python -m pip install --upgrade pip
          pip install -r requirements.txt || echo "no requirements file"

      - name: Run tests
        run: |
          pytest --maxfail=1 --disable-warnings -q
```

* Triggers on all pushes and pull requests
* Blocks PRs if tests fail

---

