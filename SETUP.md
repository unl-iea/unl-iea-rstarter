
# 🚀 Project Setup Guide for `unl-iea-rstarter`

This guide walks you through setting up a new R project using the `unl-iea-rstarter` GitHub template.

---

## 1. Create a New Repository from the Template

1. Navigate to the [`unl-iea-rstarter`](https://github.com/YOUR_ORG/unl-iea-rstarter) repository.
2. Click **"Use this template"** at the top of the page.
3. Choose **"Create a new repository"**.
4. Fill in the repository name, description, and visibility.
5. Click **"Create repository from template"**.

---

## 2. Customize Your Repository

- Update `README.md` with your project name and purpose.
- Remove or modify example files as needed.
- Add your R scripts, data, and documentation.

---

## 3. Enable GitHub Copilot with Agent Instructions

- Open `.github/ISSUE_TEMPLATE/copilot-agent-template.md`.
- Customize the instructions to reflect your project goals.
- Use these instructions as context when prompting GitHub Copilot.

Example prompt:
> "Use tidyverse style and lintr for all R scripts. Follow the project structure and testing conventions outlined in the starter template."

---

## 4. Use Markdown Task Guides

Refer to the included markdown files for common tasks:

- `linting-r-files.md`
- `tidyverse-style.md`
- `test-coverage.md`
- `unit-testing.md`
- `dependency-management.md`
- `documentation.md`
- `ci-cd.md`
- `data-validation.md`
- `package-checks.md`
- `reproducible-reports.md`

---

## 5. Restore Project Environment with renv

If `renv.lock` is present:

```r
install.packages("renv")
renv::restore()
```

This installs all required packages automatically.

---

## 6. Run GitHub Actions for Checks and Tests

GitHub Actions are pre-configured to run R CMD check and tests:

- Triggered on push or pull request to `main`
- Located in `.github/workflows/R-CMD-check.yaml`

---

## 7. Optional: Set Up Pre-Commit Hooks

Use `precommit` to enforce linting and styling before commits:

```r
install.packages("precommit")
precommit::use_precommit()
```

This adds a `.pre-commit-config.yaml` and sets up hooks.

---

Happy coding! 🎉
