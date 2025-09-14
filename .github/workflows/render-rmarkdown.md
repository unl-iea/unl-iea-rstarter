name: Render R Markdown

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  render:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repo
        uses: actions/checkout@v3

      - name: Set up R
        uses: r-lib/actions/setup-r@v2

      - name: Install dependencies
        run: |
          install.packages(c("rmarkdown", "knitr", "tidyverse", "brms", "bayesplot", "here"))

      - name: Render R Markdown
        run: |
          Rscript -e "rmarkdown::render('docs/report.Rmd', output_format = 'html_document')"

      - name: Upload rendered report
        uses: actions/upload-artifact@v3
        with:
          name: rendered-report
          path: docs/report.html
