# Linting R Files with lintr

## Overview
Use [`lintr`](https://github.com/r-lib/lintr) to check R code for style issues and potential errors.

## Setup

Install `lintr` if not already installed:

```r
install.packages("lintr")
```

## Usage

To lint a single file:

```r
lintr::lint("script.R")
```

To lint all R files in a directory:

```r
files <- list.files("R", pattern = \"\.R$\", full.names = TRUE)
lapply(files, lintr::lint)
```

## GitHub Copilot Prompt

> "Write a script to lint all R files in the `R/` directory using the `lintr` package."

## Notes

- Customize linters using `lintr::with_defaults()`.
- Consider adding a `.lintr` config file for project-specific rules.
