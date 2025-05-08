
## 3.CD Pipeline: Release Artifact

### Artifact Deployment (to `dist/` folder)

Extend `ci.yml` with:

```yaml
  deploy:
    if: github.ref == 'refs/heads/main'
    needs: test
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v3

      - name: Build package
        run: |
          python setup.py sdist bdist_wheel || echo "No setup.py"

      - name: Upload artifact
        uses: actions/upload-artifact@v3
        with:
          name: smart-healthcare-dist
          path: dist/
```

* Runs **only** on main
* Stores distributable wheel/archive

---


