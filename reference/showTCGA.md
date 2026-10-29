# Show TCGA data structure by Project ID or ALL

This can used to check if data type or file type exist in one or more
projects by hand.

## Usage

``` r
showTCGA(project = "all")
```

## Arguments

- project:

  a character vector. Can be "all" or one or more of TCGA Project IDs.

## Value

a `data.frame` including project data structure information.

## See also

[`availTCGA()`](https://docs.ropensci.org/UCSCXenaTools/reference/availTCGA.md)

## Author

Shixiang Wang <w_shixiang@163.com>

## Examples

``` r
# \donttest{
showTCGA("all")
#> # A tibble: 737 × 3
#>    ProjectID DataType                FileType                                 
#>    <chr>     <chr>                   <chr>                                    
#>  1 OV        DNA Methylation         Methylation27K                           
#>  2 OV        DNA Methylation         Methylation450K                          
#>  3 OV        Gene Level Copy Number  Gistic2                                  
#>  4 OV        Phenotype               Clinical Information                     
#>  5 OV        Protein Expression RPPA RPPA normalized by RBN                   
#>  6 OV        Gene Expression Array   Affymetrix U133A Microarray              
#>  7 OV        Gene Expression RNASeq  IlluminaHiSeq RNASeqV2 in percentile rank
#>  8 OV        Gene Expression RNASeq  IlluminaHiSeq RNASeqV2 pancan normalized 
#>  9 OV        Gene Expression RNASeq  IlluminaHiSeq RNASeqV2                   
#> 10 OV        Gene Expression RNASeq  IlluminaHiSeq RNASeq                     
#> # ℹ 727 more rows
# }
```
