# Documentation with roxygen2

## Overview
Use `roxygen2` to document R functions and generate help files.

## Setup

Install `roxygen2`:

```r
install.packages("roxygen2")
```

## Usage

Add documentation above a function:

```r
#' Add two numbers
#'
#' @param x First number
#' @param y Second number
#' @return Sum of x and y
#' @export
add <- function(x, y) {
  x + y
}
```

Generate documentation:

```r
roxygen2::roxygenise()
```

## GitHub Copilot Prompt

> "Document a function that adds two numbers using roxygen2."
