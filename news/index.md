# Changelog

## UCSCXenaTools 1.7.0

CRAN release: 2026-02-06

- Totally 2314 datasets are included in the current list.
- Removed gdcHubV18 as it is expired and not available.
- Removed hiplot support as the server is down.

## UCSCXenaTools 1.6.2

- Filtered probe names to exclude `ENSGR%` pattern (Thanks to Brian
  Craft and Mary Goldman).

## UCSCXenaTools 1.6.1

CRAN release: 2025-08-21

- Added new single cell hub url.
- Added docs for dynamics.

## UCSCXenaTools 1.6.0

- Totally 2511 datasets are included in the current list.
- Single cell hub was found disabled.
- GDC hub was completely updated. The old GDC hub has been renamed to
  gdcHubV18.

## UCSCXenaTools 1.5.0

- Bugs fixed.
- Removed useless action or check config files.
- Removed the `XenaShiny()` function to reduce the dependencies.
- Updated XenaData. Only minor datasets change found from previous data
  release.
- Hiplot mirror is down, so we removed its usage in documentation (not
  delete internal code).
- Added two new queries from xenaPython.

## UCSCXenaTools 1.4.8

CRAN release: 2022-06-20

- Updated to latest Xena dataset list.

## UCSCXenaTools 1.4.7

CRAN release: 2021-09-15

- 3 datasets were added into `XenaData`.

``` r
[1] "TCGA_survival_data_2.txt"                                  
[2] "clinical_CellLinePolyA_21.06_2021-06-15.tsv"               
[3] "CellLinePolyA_21.06_hugo_log2tpm_58581genes_2021-06-15.tsv"
```

- Added support for gene symbol checking and data cache in
  [`fetch()`](https://docs.ropensci.org/UCSCXenaTools/reference/fetch.md).

## UCSCXenaTools 1.4.6

CRAN release: 2021-07-17

- Added code to check hiplot server status.
- Fixed check warnings to follow CRAN policy
  ([\#36](https://github.com/ropensci/UCSCXenaTools/issues/36)).

## UCSCXenaTools 1.4.5

CRAN release: 2021-05-27

- Fixed the download bug for pan-cancer data hub due to unvalid URL.
  `url_encode()` is added internally to transform reserved characters
  (`/` is kept).
- Fixed the download bug because UCSCXenaShiny mutate the result of
  [`XenaQuery()`](https://docs.ropensci.org/UCSCXenaTools/reference/XenaQuery.md)
  and thus change the column number. This bug will not affect XenaTools
  itself.

## UCSCXenaTools 1.4.4

CRAN release: 2021-04-06

- Fixed the download bug because UCSCXenaShiny mutate the result of
  [`XenaQuery()`](https://docs.ropensci.org/UCSCXenaTools/reference/XenaQuery.md)
  and thus change the column order. This bug will not affect XenaTools
  itself.

## UCSCXenaTools 1.4.3

CRAN release: 2021-03-22

- Implemented using hiplot for
  [`fetch()`](https://docs.ropensci.org/UCSCXenaTools/reference/fetch.md)
  functions.

## UCSCXenaTools 1.4.1 (1.4.2)

- Removed unpublished Xena hub TDI.

## UCSCXenaTools 1.4.0

CRAN release: 2021-01-19

- Supported downloading data from Hiplot mirror site
  (`https://xena.hiplot.com.cn/`).

## UCSCXenaTools 1.3.6

CRAN release: 2020-11-23

- Fixed a bug about try times for data download.
- Make sure a message instead of an error will be returned if download
  process failed.

## UCSCXenaTools 1.3.5

CRAN release: 2020-11-14

- Added TDI data Hub containing 9 new datasets.

## UCSCXenaTools 1.3.4

CRAN release: 2020-09-30

- Updated UCSC Xena datasets, now 1670 datasets available.

## UCSCXenaTools 1.3.3

CRAN release: 2020-08-05

- Added
  [`fetch_sparse_values()`](https://docs.ropensci.org/UCSCXenaTools/reference/fetch.md)
  function.
- Updated treehouse URL.
- Added treehouse datasets.

## UCSCXenaTools 1.3.2

CRAN release: 2020-07-14

- Fixed bug about an error happened when querying mutation data.
- Dropped “Treehouse” data hub.
- Updated code to update Xena hub datasets.

## UCSCXenaTools 1.3.1

CRAN release: 2020-03-18

- Added `max_try` option in query and download functions, so they can
  handle internet connection issue better

## UCSCXenaTools 1.3.0

CRAN release: 2020-02-26

- Added a new data hub: PCAWG Xena Hub
  ([\#24](https://github.com/ropensci/UCSCXenaTools/issues/24)).
- Added a new data hub: Kids First Xena Hub
  ([\#24](https://github.com/ropensci/UCSCXenaTools/issues/24)).
- Updated data update function more robustly.
