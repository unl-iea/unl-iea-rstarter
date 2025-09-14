# Unit Testing with testthat

## Overview
Use `testthat` to write and run unit tests for R functions.

## Setup

Install `testthat`:

```r
install.packages("testthat")
```

## Usage

Create a test file in `tests/testthat/test-myfunction.R`:

```r
test_that("myfunction returns correct value", {
  expect_equal(myfunction(2), 4)
})
```

Run all tests:

```r
testthat::test_dir("tests/testthat")
```

## GitHub Copilot Prompt

> "Write a unit test for a function that doubles a number using `testthat`."

## Notes

- Use `usethis::use_testthat()` to set up testing infrastructure.
