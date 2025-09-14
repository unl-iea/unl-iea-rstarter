# Applying Tidyverse Style Guide

## Overview
Use `styler` to format R code according to the tidyverse style guide.

## Setup

Install `styler`:

```r
install.packages("styler")
```

## Usage

To style a single file:

```r
styler::style_file("script.R")
```

To style all R files in a directory:

```r
styler::style_dir("R")
```

## GitHub Copilot Prompt

> "Format all R scripts in the `R/` folder using tidyverse style with the `styler` package."

## Notes

- You can use `styler::style_pkg()` to style an entire package.
- Add a pre-commit hook to enforce styling automatically.
