# Get TCGA Common Data Sets by Project ID and Property

This is the most useful function for user to download common TCGA
datasets, it is similar to `getFirehoseData` function in `RTCGAToolbox`
package.

## Usage

``` r
getTCGAdata(
  project = NULL,
  clinical = TRUE,
  download = FALSE,
  forceDownload = FALSE,
  destdir = tempdir(),
  mRNASeq = FALSE,
  mRNAArray = FALSE,
  mRNASeqType = "normalized",
  miRNASeq = FALSE,
  exonRNASeq = FALSE,
  RPPAArray = FALSE,
  ReplicateBaseNormalization = FALSE,
  Methylation = FALSE,
  MethylationType = c("27K", "450K"),
  GeneMutation = FALSE,
  SomaticMutation = FALSE,
  GisticCopyNumber = FALSE,
  Gistic2Threshold = TRUE,
  CopyNumberSegment = FALSE,
  RemoveGermlineCNV = TRUE,
  ...
)
```

## Arguments

- project:

  default is `NULL`. Should be one or more of TCGA project id (character
  vector) provided by Xena. See all available project id, please use
  `availTCGA("ProjectID")`.

- clinical:

  logical. if `TRUE`, download clinical information. Default is `TRUE`.

- download:

  logical. if `TRUE`, download data, otherwise return a result list
  include data information. Default is `FALSE`. You can set this to
  `FALSE` if you want to check what you will download or use other
  function provided by `UCSCXenaTools` to filter result datasets you
  want to download.

- forceDownload:

  logical. if `TRUE`, force to download files no matter if exist.
  Default is `FALSE`.

- destdir:

  specify a location to store download data. Default is system temp
  directory.

- mRNASeq:

  logical. if `TRUE`, download mRNASeq data. Default is `FALSE`.

- mRNAArray:

  logical. if `TRUE`, download mRNA microarray data. Default is `FALSE`.

- mRNASeqType:

  character vector. Can be one, two or three in
  `c("normalized", "pancan normalized", "percentile")`.

- miRNASeq:

  logical. if `TRUE`, download miRNASeq data. Default is `FALSE`.

- exonRNASeq:

  logical. if `TRUE`, download exon RNASeq data. Default is `FALSE`.

- RPPAArray:

  logical. if `TRUE`, download RPPA data. Default is `FALSE`.

- ReplicateBaseNormalization:

  logical. if `TRUE`, download RPPA data by Replicate Base Normalization
  (RBN). Default is `FALSE`.

- Methylation:

  logical. if `TRUE`, download DNA Methylation data. Default is `FALSE`.

- MethylationType:

  character vector. Can be one or two in `c("27K", "450K")`.

- GeneMutation:

  logical. if `TRUE`, download gene mutation data. Default is `FALSE`.

- SomaticMutation:

  logical. if `TRUE`, download somatic mutation data. Default is
  `FALSE`.

- GisticCopyNumber:

  logical. if `TRUE`, download Gistic2 Copy Number data. Default is
  `FALSE`.

- Gistic2Threshold:

  logical. if `TRUE`, download Threshold Gistic2 data. Default is
  `TRUE`.

- CopyNumberSegment:

  logical. if `TRUE`, download Copy Number Segment data. Default is
  `FALSE`.

- RemoveGermlineCNV:

  logical. if `TRUE`, download Copy Number Segment data which has
  removed germline copy number variation. Default is `TRUE`.

- ...:

  other argument to `download.file` function

## Value

if `download=TRUE`, return `data.frame` from `XenaDownload`, otherwise
return a list including `XenaHub` object and datasets information

## Details

TCGA Common Data Sets are frequently used for biological analysis. To
make easier to achieve these data, this function provide really easy
options to choose datasets and behavior. All availble information about
datasets of TCGA can access vis
[`availTCGA()`](https://docs.ropensci.org/UCSCXenaTools/reference/availTCGA.md)
and check with
[`showTCGA()`](https://docs.ropensci.org/UCSCXenaTools/reference/showTCGA.md).

## Author

Shixiang Wang <w_shixiang@163.com>

## Examples

``` r
###### get data, but not download

# 1 choose project and data types you wanna download
getTCGAdata(project = "LUAD", mRNASeq = TRUE, mRNAArray = TRUE,
mRNASeqType = "normalized", miRNASeq = TRUE, exonRNASeq = TRUE,
RPPAArray = TRUE, Methylation = TRUE, MethylationType = "450K",
GeneMutation = TRUE, SomaticMutation = TRUE)
#> $Xena
#> class: XenaHub 
#> hosts():
#>   https://tcga.xenahubs.net
#> cohorts() (1 total):
#>   TCGA Lung Adenocarcinoma (LUAD)
#> datasets() (7 total):
#>   TCGA.LUAD.sampleMap/HumanMethylation450
#>   TCGA.LUAD.sampleMap/HiSeqV2
#>   TCGA.LUAD.sampleMap/miRNA_HiSeq_gene
#>   ...
#>   TCGA.LUAD.sampleMap/AgilentG4502A_07_3
#>   TCGA.LUAD.sampleMap/HiSeqV2_exon
#> 
#> $DataInfo
#> # A tibble: 7 × 20
#>   XenaHosts XenaHostNames XenaCohorts XenaDatasets SampleCount DataSubtype Label
#>   <chr>     <chr>         <chr>       <chr>              <int> <chr>       <chr>
#> 1 https://… tcgaHub       TCGA Lung … TCGA.LUAD.s…         492 DNA methyl… Meth…
#> 2 https://… tcgaHub       TCGA Lung … TCGA.LUAD.s…         576 gene expre… Illu…
#> 3 https://… tcgaHub       TCGA Lung … TCGA.LUAD.s…         495 miRNA matu… Illu…
#> 4 https://… tcgaHub       TCGA Lung … TCGA.LUAD.s…         706 phenotype   Phen…
#> 5 https://… tcgaHub       TCGA Lung … TCGA.LUAD.s…         365 protein ex… RPPA 
#> 6 https://… tcgaHub       TCGA Lung … TCGA.LUAD.s…          33 gene expre… Agil…
#> 7 https://… tcgaHub       TCGA Lung … TCGA.LUAD.s…         576 exon expre… Illu…
#> # ℹ 13 more variables: Type <chr>, AnatomicalOrigin <chr>, SampleType <chr>,
#> #   Tags <chr>, ProbeMap <chr>, LongTitle <chr>, Citation <chr>, Version <chr>,
#> #   Unit <chr>, Platform <chr>, ProjectID <chr>, DataType <chr>, FileType <chr>
#> 

# 2 only choose 'LUAD' and its clinical data
getTCGAdata(project = "LUAD")
#> $Xena
#> class: XenaHub 
#> hosts():
#>   https://tcga.xenahubs.net
#> cohorts() (1 total):
#>   TCGA Lung Adenocarcinoma (LUAD)
#> datasets() (1 total):
#>   TCGA.LUAD.sampleMap/LUAD_clinicalMatrix
#> 
#> $DataInfo
#> # A tibble: 1 × 20
#>   XenaHosts XenaHostNames XenaCohorts XenaDatasets SampleCount DataSubtype Label
#>   <chr>     <chr>         <chr>       <chr>              <int> <chr>       <chr>
#> 1 https://… tcgaHub       TCGA Lung … TCGA.LUAD.s…         706 phenotype   Phen…
#> # ℹ 13 more variables: Type <chr>, AnatomicalOrigin <chr>, SampleType <chr>,
#> #   Tags <chr>, ProbeMap <chr>, LongTitle <chr>, Citation <chr>, Version <chr>,
#> #   Unit <chr>, Platform <chr>, ProjectID <chr>, DataType <chr>, FileType <chr>
#> 
if (FALSE) { # \dontrun{
###### download datasets

# 3 download clinical datasets of LUAD and LUSC
getTCGAdata(project = c("LUAD", "LUSC"), clinical = TRUE, download = TRUE)

# 4 download clinical, RPPA and gene mutation datasets of LUAD and LUSC
# getTCGAdata(project = c("LUAD", "LUSC"), clinical = TRUE, RPPAArray = TRUE, GeneMutation = TRUE)
} # }
```
