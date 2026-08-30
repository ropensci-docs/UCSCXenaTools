# View Info of Dataset or Cohort at UCSC Xena Website Using Web browser

This will open dataset/cohort link of UCSC Xena in user's default
browser.

## Usage

``` r
XenaBrowse(x, type = c("dataset", "cohort"), multiple = FALSE)
```

## Arguments

- x:

  a
  [XenaHub](https://docs.ropensci.org/UCSCXenaTools/reference/XenaHub.md)
  object.

- type:

  one of "dataset" and "cohort".

- multiple:

  if `TRUE`, browse multiple links instead of throwing error.

## Examples

``` r
# \donttest{
XenaGenerate(subset = XenaHostNames == "tcgaHub") %>%
  XenaFilter(filterDatasets = "clinical") %>%
  XenaFilter(filterDatasets = "LUAD") -> to_browse
# }
```
