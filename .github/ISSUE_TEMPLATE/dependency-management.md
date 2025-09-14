# Dependency Management with renv

## Overview
Use `renv` to manage R package dependencies in isolated environments.

## Setup

Install `renv`:

```r
install.packages("renv")
```

## Usage

Initialize renv:

```r
renv::init()
```

Snapshot dependencies:

```r
renv::snapshot()
```

Restore environment:

```r
renv::restore()
```

## GitHub Copilot Prompt

> "Set up renv for my R project and snapshot current dependencies."

## Notes

- Commit `renv.lock` to version control.
