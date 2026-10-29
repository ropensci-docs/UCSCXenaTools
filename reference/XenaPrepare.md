# Prepare (Load) Downloaded Datasets to R

Prepare (Load) Downloaded Datasets to R

## Usage

``` r
XenaPrepare(
  objects,
  objectsName = NULL,
  use_chunk = FALSE,
  chunk_size = 100,
  subset_rows = TRUE,
  select_cols = TRUE,
  callback = NULL,
  comment = "#",
  na = c("", "NA", "[Discrepancy]"),
  ...
)
```

## Arguments

- objects:

  a object of character vector or data.frame. If `objects` is
  data.frame, it should be returned object of
  [XenaDownload](https://docs.ropensci.org/UCSCXenaTools/reference/XenaDownload.md)
  function. More easier way is that objects can be character vector
  specify local files/directory and download urls.

- objectsName:

  specify names for elements of return object, i.e. names of list

- use_chunk:

  default is `FALSE`. If you want to select subset of original data,
  please set it to `TRUE` and specify corresponding arguments:
  `chunk_size`, `select_direction`, `select_names`, `callback`.

- chunk_size:

  the number of rows to include in each chunk

- subset_rows:

  logical expression indicating elements or rows to keep: missing values
  are taken as false. `x` can be a representation of data frame you
  wanna do subset operation. Of note, the first colname of most of
  datasets in Xena will be set to "sample", you can use it to select
  rows.

- select_cols:

  expression, indicating columns to select from a data frame. 'x' can be
  a representation of data frame you wanna do subset operation, e.g.
  `select_cols = colnames(x)[1:3]` will keep only first to third column.

- callback:

  a function to call on each chunk, default is `NULL`, this option will
  overvide operations of subset_rows and select_cols.

- comment:

  a character specify comment rows in files

- na:

  a character vectory specify `NA` values in files

- ...:

  other arguments transfer to `read_tsv` function or `read_tsv_chunked`
  function (when `use_chunk` is `TRUE`) of `readr` package.

## Value

a list contains file data, which in way of tibbles

## Author

Shixiang Wang <w_shixiang@163.com>

## Examples

``` r
if (FALSE) { # \dontrun{
xe = XenaGenerate(subset = XenaHostNames == "tcgaHub")
hosts(xe)
xe_query = XenaQuery(xe)

xe_download = XenaDownload(xe_query)
dat = XenaPrepare(xe_download)
} # }
```
