# Generate and Subset a XenaHub Object from 'XenaData'

Generate and Subset a XenaHub Object from 'XenaData'

## Usage

``` r
XenaGenerate(XenaData = UCSCXenaTools::XenaData, subset = TRUE)
```

## Arguments

- XenaData:

  a `data.frame`. Default is `data(XenaData)`. The input of this option
  can only be `data(XenaData)` or its subset.

- subset:

  logical expression indicating elements or rows to keep.

## Value

a
[XenaHub](https://docs.ropensci.org/UCSCXenaTools/reference/XenaHub.md)
object.

## Author

Shixiang Wang <w_shixiang@163.com>

## Examples

``` r
# 1 get all datasets
XenaGenerate()
#> class: XenaHub 
#> hosts():
#>   https://ucscpublic.xenahubs.net
#>   https://tcga.xenahubs.net
#>   https://gdc.xenahubs.net
#>   https://icgc.xenahubs.net
#>   https://toil.xenahubs.net
#>   https://pancanatlas.xenahubs.net
#>   https://xena.treehouse.gi.ucsc.edu:443
#>   https://pcawg.xenahubs.net
#>   https://atacseq.xenahubs.net
#>   https://previewsinglecell.xenahubs.net
#>   https://kidsfirst.xenahubs.net
#> cohorts() (255 total):
#>   Breast Cancer Cell Lines (Neve 2006)
#>   Glioma (Kotliarov 2006)
#>   Lung Cancer CGH (Weir 2007)
#>   ...
#>   Pediatric Brain Tumor Atlas: PNOC
#>   Pediatric Brain Tumor Atlas: CBTTC
#> datasets() (2314 total):
#>   ucsfNeve_public/ucsfNeveExp_genomicMatrix
#>   ucsfNeve_public/ucsfNeve_public_clinicalMatrix
#>   kotliarov2006_public/kotliarov2006_genomicMatrix
#>   ...
#>   CBTTC/CBTTC_Phosphoproteome.phosphosite.tmt11.tsv
#>   CBTTC/CBTTC_WGS-simple-variants_strelka.txt
# 2 get TCGA BRCA
XenaGenerate(subset = XenaCohorts == "TCGA Breast Cancer (BRCA)")
#> class: XenaHub 
#> hosts():
#>   https://tcga.xenahubs.net
#> cohorts() (1 total):
#>   TCGA Breast Cancer (BRCA)
#> datasets() (24 total):
#>   RABIT/separate_processed/RABIT_BRCA.HiSeq
#>   RABIT/separate_processed/RABIT_BRCA.Agilent
#>   RABIT/separate_processed/RABIT_BRCA.HiSeq.V2
#>   ...
#>   PanCan33_ssGSEA_1387GeneSets_NonZero_sample_level_Z/BRCA_PanCan33_ssGSEA_1387GeneSets_NonZero_sample_level_Z.txt
#>   survival/BRCA_survival.txt
# 3 get all datasets containing BRCA
XenaGenerate(subset = grepl("BRCA", XenaCohorts))
#> class: XenaHub 
#> hosts():
#>   https://tcga.xenahubs.net
#>   https://gdc.xenahubs.net
#>   https://atacseq.xenahubs.net
#> cohorts() (2 total):
#>   TCGA Breast Cancer (BRCA)
#>   GDC TCGA Breast Cancer (BRCA)
#> datasets() (48 total):
#>   RABIT/separate_processed/RABIT_BRCA.HiSeq
#>   RABIT/separate_processed/RABIT_BRCA.Agilent
#>   RABIT/separate_processed/RABIT_BRCA.HiSeq.V2
#>   ...
#>   brca/pam50
#>   brca/TCGA-BRCA.methylation450.tsv
```
