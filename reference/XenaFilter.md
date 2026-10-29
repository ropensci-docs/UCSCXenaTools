# Filter a XenaHub Object

One of main functions in **UCSCXenatools**. It is used to filter
`XenaHub` object according to cohorts, datasets. All datasets can be
found at <https://xenabrowser.net/datapages/>.

## Usage

``` r
XenaFilter(
  x,
  filterCohorts = NULL,
  filterDatasets = NULL,
  ignore.case = TRUE,
  ...
)
```

## Arguments

- x:

  a
  [XenaHub](https://docs.ropensci.org/UCSCXenaTools/reference/XenaHub.md)
  object

- filterCohorts:

  default is `NULL`. A character used to filter cohorts, regular
  expression is supported.

- filterDatasets:

  default is `NULL`. A character used to filter datasets, regular
  expression is supported.

- ignore.case:

  if `FALSE`, the pattern matching is case sensitive and if `TRUE`, case
  is ignored during matching.

- ...:

  other arguments except `value` passed to
  [`base::grep()`](https://rdrr.io/r/base/grep.html).

## Value

a `XenaHub` object

## Author

Shixiang Wang <w_shixiang@163.com>

## Examples

``` r
# operate TCGA datasets
xe = XenaGenerate(subset = XenaHostNames == "tcgaHub")
xe
#> class: XenaHub 
#> hosts():
#>   https://tcga.xenahubs.net
#> cohorts() (38 total):
#>   TCGA Ovarian Cancer (OV)
#>   TCGA Kidney Clear Cell Carcinoma (KIRC)
#>   TCGA Lower Grade Glioma (LGG)
#>   ...
#>   TCGA Colon Cancer (COAD)
#>   TCGA Formalin Fixed Paraffin-Embedded Pilot Phase II (FPPP)
#> datasets() (715 total):
#>   TCGA.OV.sampleMap/HumanMethylation27
#>   TCGA.OV.sampleMap/HumanMethylation450
#>   TCGA.OV.sampleMap/Gistic2_CopyNumber_Gistic2_all_data_by_genes
#>   ...
#>   TCGA.FPPP.sampleMap/miRNA_HiSeq_gene
#>   TCGA.FPPP.sampleMap/FPPP_clinicalMatrix
# get all names of clinical data
xe2 = XenaFilter(xe, filterDatasets = "clinical")
datasets(xe2)
#>  [1] "TCGA.OV.sampleMap/OV_clinicalMatrix"            
#>  [2] "TCGA.KIRC.sampleMap/KIRC_clinicalMatrix"        
#>  [3] "TCGA.LGG.sampleMap/LGG_clinicalMatrix"          
#>  [4] "TCGA.KIRP.sampleMap/KIRP_clinicalMatrix"        
#>  [5] "TCGA.CHOL.sampleMap/CHOL_clinicalMatrix"        
#>  [6] "TCGA.COADREAD.sampleMap/COADREAD_clinicalMatrix"
#>  [7] "TCGA.ACC.sampleMap/ACC_clinicalMatrix"          
#>  [8] "TCGA.CESC.sampleMap/CESC_clinicalMatrix"        
#>  [9] "TCGA.READ.sampleMap/READ_clinicalMatrix"        
#> [10] "TCGA.SARC.sampleMap/SARC_clinicalMatrix"        
#> [11] "TCGA.DLBC.sampleMap/DLBC_clinicalMatrix"        
#> [12] "TCGA.PRAD.sampleMap/PRAD_clinicalMatrix"        
#> [13] "TCGA.LUNG.sampleMap/LUNG_clinicalMatrix"        
#> [14] "TCGA.LIHC.sampleMap/LIHC_clinicalMatrix"        
#> [15] "TCGA.KICH.sampleMap/KICH_clinicalMatrix"        
#> [16] "TCGA.HNSC.sampleMap/HNSC_clinicalMatrix"        
#> [17] "TCGA.PCPG.sampleMap/PCPG_clinicalMatrix"        
#> [18] "TCGA.ESCA.sampleMap/ESCA_clinicalMatrix"        
#> [19] "TCGA.THCA.sampleMap/THCA_clinicalMatrix"        
#> [20] "TCGA.LUAD.sampleMap/LUAD_clinicalMatrix"        
#> [21] "TCGA.LAML.sampleMap/LAML_clinicalMatrix"        
#> [22] "TCGA.BLCA.sampleMap/BLCA_clinicalMatrix"        
#> [23] "TCGA.SKCM.sampleMap/SKCM_clinicalMatrix"        
#> [24] "TCGA.LUSC.sampleMap/LUSC_clinicalMatrix"        
#> [25] "TCGA.TGCT.sampleMap/TGCT_clinicalMatrix"        
#> [26] "TCGA.PAAD.sampleMap/PAAD_clinicalMatrix"        
#> [27] "TCGA.GBM.sampleMap/GBM_clinicalMatrix"          
#> [28] "TCGA.STAD.sampleMap/STAD_clinicalMatrix"        
#> [29] "TCGA.MESO.sampleMap/MESO_clinicalMatrix"        
#> [30] "TCGA.UVM.sampleMap/UVM_clinicalMatrix"          
#> [31] "TCGA.GBMLGG.sampleMap/GBMLGG_clinicalMatrix"    
#> [32] "TCGA.THYM.sampleMap/THYM_clinicalMatrix"        
#> [33] "TCGA.UCEC.sampleMap/UCEC_clinicalMatrix"        
#> [34] "TCGA.BRCA.sampleMap/BRCA_clinicalMatrix"        
#> [35] "TCGA.UCS.sampleMap/UCS_clinicalMatrix"          
#> [36] "TCGA.COAD.sampleMap/COAD_clinicalMatrix"        
#> [37] "TCGA.FPPP.sampleMap/FPPP_clinicalMatrix"        
```
