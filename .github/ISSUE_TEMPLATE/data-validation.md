# Data Validation with validate and assertr

## Overview
Use `validate` or `assertr` to check data integrity and enforce rules.

## Setup

Install packages:

```r
install.packages(c("validate", "assertr"))
```

## Usage

Using `validate`:

```r
rules <- validator(age >= 0, income >= 0)
cf <- confront(data, rules)
summary(cf)
```

Using `assertr`:

```r
data %>%
  verify(age >= 0) %>%
  assert(in_range(0, 100), age)
```

## GitHub Copilot Prompt

> "Validate that age is non-negative and income is positive using `validate`."
