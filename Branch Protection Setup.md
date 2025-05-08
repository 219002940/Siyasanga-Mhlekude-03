# Assignment 13: Implementing CI/CD with GitHub Actions

## Objective

Establish a CI/CD pipeline for the Smart Health Care Monitoring System using GitHub Actions. This ensures automated testing, artifact creation, and branch protection to prevent errors from reaching the `main` branch.

---

## 1. Branch Protection Setup

### GitHub Steps:

1. Navigate to **Settings > Branches > Add Rule**
2. Apply to `main` branch.
3. Enable the following:

   * Require pull request reviews before merging (min. 1 approval)
   * Require status checks to pass (CI must succeed)
   * Block direct pushes to `main`

### Why It Matters

* **Avoids Breaking Production:** Prevents merging untested or unauthorized changes.
* **Enforces Quality:** Requires code reviews and passing CI builds.
* **Industry Practice:** Aligns with secure software delivery standards.

Documented in: [`PROTECTION.md`](PROTECTION.md)

---


