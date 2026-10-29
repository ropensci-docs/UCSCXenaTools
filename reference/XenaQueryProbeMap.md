# Query ProbeMap URL of Datasets

If dataset has no ProbeMap, it will be ignored.

## Usage

``` r
XenaQueryProbeMap(x)
```

## Arguments

- x:

  a
  [XenaHub](https://docs.ropensci.org/UCSCXenaTools/reference/XenaHub.md)
  object

## Value

a `data.frame` contains hosts, datasets and url

## Author

Shixiang Wang <w_shixiang@163.com>

## Examples

``` r
xe = XenaGenerate(subset = XenaHostNames == "tcgaHub")
hosts(xe)
#> [1] "https://tcga.xenahubs.net"
if (FALSE) { # \dontrun{
xe_query = XenaQueryProbeMap(xe)
} # }
```
