# Get Samples of a XenaHub object according to 'by' and 'how' action arguments

One is often interested in identifying samples or features present in
each data set, or shared by all data sets, or present in any of several
data sets. Identifying these samples, including samples in arbitrarily
chosen data sets.

## Usage

``` r
samples(
  x,
  i = character(),
  by = c("hosts", "cohorts", "datasets"),
  how = c("each", "any", "all")
)
```

## Arguments

- x:

  a
  [XenaHub](https://docs.ropensci.org/UCSCXenaTools/reference/XenaHub.md)
  object

- i:

  default is a empty character, it is used to specify the host, cohort
  or dataset by `by` option otherwise info will be automatically
  extracted by code

- by:

  a character specify `by` action

- how:

  a character specify `how` action

## Value

a list include samples

## Examples

``` r
if (FALSE) { # \dontrun{
xe = XenaHub(cohorts = "Cancer Cell Line Encyclopedia (CCLE)")
# samples in each dataset, first host
x = samples(xe, by="datasets", how="each")[[1]]
lengths(x)        # data sets in ccle cohort on first (only) host
} # }
```
