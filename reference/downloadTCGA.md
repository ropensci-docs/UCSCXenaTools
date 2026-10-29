# Easily Download TCGA Data by Several Options

TCGA is a very useful database and here we provide this function to
download TCGA (include TCGA Pancan) datasets in human-friendly way.
Users who are not familiar with R operation will benefit from this.

## Usage

``` r
downloadTCGA(
  project = NULL,
  data_type = NULL,
  file_type = NULL,
  destdir = tempdir(),
  force = FALSE,
  ...
)
```

## Arguments

- project:

  default is `NULL`. Should be one or more of TCGA project id (character
  vector) provided by Xena. See all available project id, please use
  `availTCGA("ProjectID")`.

- data_type:

  default is `NULL`. Should be a character vector specify data type. See
  all available data types by `availTCGA("DataType")`.

- file_type:

  default is `NULL`. Should be a character vector specify file type. See
  all available file types by `availTCGA("FileType")`.

- destdir:

  specify a location to store download data. Default is system temp
  directory.

- force:

  logical. if `TRUE`, force to download data no matter whether files
  exist. Default is `FALSE`.

- ...:

  other argument to `download.file` function

## Value

same as
[`XenaDownload()`](https://docs.ropensci.org/UCSCXenaTools/reference/XenaDownload.md)
function result.

## Details

All availble information about datasets of TCGA can access vis
[`availTCGA()`](https://docs.ropensci.org/UCSCXenaTools/reference/availTCGA.md)
and check with
[`showTCGA()`](https://docs.ropensci.org/UCSCXenaTools/reference/showTCGA.md).

## See also

[`XenaQuery()`](https://docs.ropensci.org/UCSCXenaTools/reference/XenaQuery.md),
[`XenaFilter()`](https://docs.ropensci.org/UCSCXenaTools/reference/XenaFilter.md),
[`XenaDownload()`](https://docs.ropensci.org/UCSCXenaTools/reference/XenaDownload.md),
[`XenaPrepare()`](https://docs.ropensci.org/UCSCXenaTools/reference/XenaPrepare.md),
[`availTCGA()`](https://docs.ropensci.org/UCSCXenaTools/reference/availTCGA.md),
[`showTCGA()`](https://docs.ropensci.org/UCSCXenaTools/reference/showTCGA.md)

## Author

Shixiang Wang <w_shixiang@163.com>

## Examples

``` r
if (FALSE) { # \dontrun{
# download RNASeq data (use UVM as example)
downloadTCGA(project = "UVM",
                 data_type = "Gene Expression RNASeq",
                 file_type = "IlluminaHiSeq RNASeqV2")
} # }
```
