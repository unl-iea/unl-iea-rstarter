# CI/CD with GitHub Actions for R

## Overview
Use GitHub Actions to automate testing and deployment of R projects.

## Setup

Create `.github/workflows/R-CMD-check.yaml`:

```yaml
name: R-CMD-check

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  R-CMD-check:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: r-lib/actions/setup-r@v2
      - name: Install dependencies
        run: Rscript -e "install.packages(c('devtools', 'testthat'))"
      - name: Check
        run: R CMD check .
```

## GitHub Copilot Prompt

> "Create a GitHub Actions workflow to run R CMD check on push."
