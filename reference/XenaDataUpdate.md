# Get or Update Newest Data Information of UCSC Xena Data Hubs

Get or Update Newest Data Information of UCSC Xena Data Hubs

## Usage

``` r
XenaDataUpdate(saveTolocal = TRUE)
```

## Arguments

- saveTolocal:

  logical. Whether save to local R package data directory for permanent
  use or Not.

## Value

a `data.frame` contains all datasets information of Xena.

## Author

Shixiang Wang <w_shixiang@163.com>

## Examples

``` r
if (FALSE) { # \dontrun{
XenaDataUpdate()
XenaDataUpdate(saveTolocal = TRUE)
} # }
```
