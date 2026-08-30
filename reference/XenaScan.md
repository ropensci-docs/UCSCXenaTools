# Scan all rows according to user input by a regular expression

`XenaScan()` is a function can be used before
[`XenaGenerate()`](https://docs.ropensci.org/UCSCXenaTools/reference/XenaGenerate.md).

## Usage

``` r
XenaScan(
  XenaData = UCSCXenaTools::XenaData,
  pattern = NULL,
  ignore.case = TRUE
)
```

## Arguments

- XenaData:

  a `data.frame`. Default is `data(XenaData)`. The input of this option
  can only be `data(XenaData)` or its subset.

- pattern:

  character string containing a [regular
  expression](https://rdrr.io/r/base/regex.html) (or character string
  for `fixed = TRUE`) to be matched in the given character vector.
  Coerced by [`as.character`](https://rdrr.io/r/base/character.html) to
  a character string if possible. If a character vector of length 2 or
  more is supplied, the first element is used with a warning. Missing
  values are allowed except for `regexpr`, `gregexpr` and `regexec`.

- ignore.case:

  logical. if `FALSE`, the pattern matching is *case sensitive* and if
  `TRUE`, case is ignored during matching.

## Value

a `data.frame`

## Examples

``` r

x1 <- XenaScan(pattern = "Blood")
x2 <- XenaScan(pattern = "LUNG", ignore.case = FALSE)

x1 %>%
  XenaGenerate()
#> class: XenaHub 
#> hosts():
#>   https://ucscpublic.xenahubs.net
#>   https://tcga.xenahubs.net
#>   https://previewsinglecell.xenahubs.net
#> cohorts() (7 total):
#>   Connectivity Map
#>   TARGET Acute Lymphoblastic Leukemia
#>   Pediatric tumor (Khan)
#>   ...
#>   TCGA Acute Myeloid Leukemia (LAML)
#>   HTAN CHOP_Blood
#> datasets() (33 total):
#>   cmap/rankMatrix_reverse
#>   TARGET_ALL/TARGETcnv_genomicMatrix
#>   TARGET_ALL/TARGETexp_genomicMatrix
#>   ...
#>   HTAN_CHOP/seurat_regrCycleHeatShockGenes_pool_18Infants_scRNA_VEG3000_updated_rename/tsne_3D.tsv
#>   HTAN_CHOP/seurat_regrCycleHeatShockGenes_pool_18Infants_scRNA_VEG3000_updated_rename/exprMatrix.tsv
x2 %>%
  XenaGenerate()
#> class: XenaHub 
#> hosts():
#>   https://tcga.xenahubs.net
#> cohorts() (1 total):
#>   TCGA Lung Cancer (LUNG)
#> datasets() (15 total):
#>   TCGA.LUNG.sampleMap/HumanMethylation27
#>   TCGA.LUNG.sampleMap/HumanMethylation450
#>   TCGA.LUNG.sampleMap/Gistic2_CopyNumber_Gistic2_all_data_by_genes
#>   ...
#>   mc3/LUNG_mc3.txt
#>   mc3_gene_level/LUNG_mc3_gene_level.txt
```
