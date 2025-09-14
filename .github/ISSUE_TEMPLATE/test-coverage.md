# Generating Test Coverage Reports

## Overview
Use `covr` to measure test coverage in R packages.

## Setup

Install `covr`:

```r
install.packages("covr")
```

## Usage

To generate coverage report:

```r
covr::package_coverage()
```

To view coverage in HTML:

```r
covr::report()
```

## GitHub Copilot Prompt

> "Generate a test coverage report for my R package using `covr` and open it in the browser."

## Notes

- Integrate with GitHub Actions for CI coverage reporting.
- Use `codecov` for badge integration.
