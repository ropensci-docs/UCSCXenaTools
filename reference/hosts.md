# Get hosts of XenaHub object

Get hosts of XenaHub object

## Usage

``` r
hosts(x)
```

## Arguments

- x:

  a
  [XenaHub](https://docs.ropensci.org/UCSCXenaTools/reference/XenaHub.md)
  object

## Value

a character vector contains hosts

## Examples

``` r
xe = XenaGenerate(subset = XenaHostNames == "tcgaHub"); hosts(xe)
#> [1] "https://tcga.xenahubs.net"
```
