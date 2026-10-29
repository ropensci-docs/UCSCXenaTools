# Generate a XenaHub Object

It is used to generate original `XenaHub` object according to hosts,
cohorts, datasets or hostName. If these arguments not specified, all
hosts and corresponding datasets will be returned as a `XenaHub` object.
All datasets can be found at <https://xenabrowser.net/datapages/>.

## Usage

``` r
XenaHub(
  hosts = xena_default_hosts(),
  cohorts = character(),
  datasets = character(),
  hostName = c("publicHub", "tcgaHub", "gdcHub", "icgcHub", "toilHub", "pancanAtlasHub",
    "treehouseHub", "pcawgHub", "atacseqHub", "singlecellHub", "kidsfirstHub", "tdiHub")
)
```

## Arguments

- hosts:

  a character vector specify UCSC Xena hosts, all available hosts can be
  found by
  [`xena_default_hosts()`](https://docs.ropensci.org/UCSCXenaTools/reference/xena_default_hosts.md)
  function. `hostName` is a more recommend option.

- cohorts:

  default is empty character vector, all cohorts will be returned.

- datasets:

  default is empty character vector, all datasets will be returned.

- hostName:

  name of host, available options can be accessed by `.xena_hosts` This
  is an easier option for user than `hosts` option. Note, this option
  will overlap `hosts`.

## Value

a XenaHub object

## Author

Shixiang Wang <w_shixiang@163.com>

## Examples

``` r
if (FALSE) { # \dontrun{
#1 query all hosts, cohorts and datasets
xe = XenaHub()
xe
#2 query only TCGA hosts
xe = XenaHub(hostName = "tcgaHub")
xe
hosts(xe)     # get hosts
cohorts(xe)   # get cohorts
datasets(xe)  # get datasets
samples(xe)   # get samples
} # }
```
