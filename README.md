# Online shoppers: browsing and purchase conversion

Group project exploring whether the association between product-page browsing time and purchase differs for new and returning visitors. This is an initial descriptive EDA; the planned logistic regression is a later step.

## Run the EDA

Open `eda.Rmd` in RStudio and click **Knit**, or run from the repository root:

```r
install.packages(c("rmarkdown", "knitr", "car")) # only if needed
rmarkdown::render("eda.Rmd") # PDF; use output_format = "html_document" for HTML
```

The report reads `data/online_shoppers_intention.csv`. It summarizes missingness, center, variability, categorical levels and frequencies, zero browsing durations, visitor groups, and descriptive purchase rates. The report uses the original full sample for data-quality tables and clearly identifies the sample after excluding the `Other` visitor type.

Added duration bin boundaries, Wilson 95% intervals, a page count–duration check, and the interaction hypothesis and baseline model. (Yichao Zhou, 11/15) [View the PDF](eda.pdf).

Added the data description, data-quality checks (duplicate rows, very long durations), pooling of sparse traffic types, the baseline model equation, and the fitted baseline with GVIFs; the report now knits to PDF. (Lutong Zou, 11/17)

The [group proposal](https://docs.google.com/document/d/1fuHlRmEPYQq1Zvb7D94DZxCQpCXNZKgZl3D_x3Gcfjk/edit?tab=t.0) describes the later model. Data provenance and attribution are in [data/README.md](data/README.md).
