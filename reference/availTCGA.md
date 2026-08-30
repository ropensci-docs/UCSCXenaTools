# Get or Check TCGA Available ProjectID, DataType and FileType

Get or Check TCGA Available ProjectID, DataType and FileType

## Usage

``` r
availTCGA(which = c("all", "ProjectID", "DataType", "FileType"))
```

## Arguments

- which:

  a character of `c("All", "ProjectID", "DataType", "FileType")`

## Author

Shixiang Wang <w_shixiang@163.com>

## Examples

``` r
# \donttest{
availTCGA("all")
#> Note not all projects have listed data types and file types, you can use showTCGA function to check if exist
#> $ProjectID
#>  [1] "OV"       "KIRC"     "LGG"      "KIRP"     "PANCAN"   "CHOL"    
#>  [7] "COADREAD" "ACC"      "CESC"     "READ"     "SARC"     "DLBC"    
#> [13] "PRAD"     "LUNG"     "LIHC"     "KICH"     "HNSC"     "PCPG"    
#> [19] "ESCA"     "THCA"     "LUAD"     "LAML"     "BLCA"     "SKCM"    
#> [25] "LUSC"     "TGCT"     "PAAD"     "GBM"      "STAD"     "MESO"    
#> [31] "UVM"      "GBMLGG"   "THYM"     "UCEC"     "BRCA"     "UCS"     
#> [37] "COAD"     "FPPP"    
#> 
#> $DataType
#>  [1] "DNA Methylation"                       
#>  [2] "Gene Level Copy Number"                
#>  [3] "Phenotype"                             
#>  [4] "Protein Expression RPPA"               
#>  [5] "Gene Expression Array"                 
#>  [6] "Gene Expression RNASeq"                
#>  [7] "Copy Number Segments"                  
#>  [8] "miRNA Mature Strand Expression RNASeq" 
#>  [9] "Exon Expression RNASeq"                
#> [10] "Transcription Factor Regulatory Impact"
#> [11] "PARADIGM Pathway Activity"             
#> [12] NA                                      
#> [13] "Gene Somatic Non-silent Mutation"      
#> [14] "Somatic Mutation"                      
#> [15] "Signatures"                            
#> [16] "iCluster"                              
#> 
#> $FileType
#>  [1] "Methylation27K"                            
#>  [2] "Methylation450K"                           
#>  [3] "Gistic2"                                   
#>  [4] "Clinical Information"                      
#>  [5] "RPPA normalized by RBN"                    
#>  [6] "Affymetrix U133A Microarray"               
#>  [7] "IlluminaHiSeq RNASeqV2 in percentile rank" 
#>  [8] "IlluminaHiSeq RNASeqV2 pancan normalized"  
#>  [9] "IlluminaHiSeq RNASeqV2"                    
#> [10] "IlluminaHiSeq RNASeq"                      
#> [11] "After remove germline cnv"                 
#> [12] "Agilent 244K Microarray"                   
#> [13] "Gistic2 thresholded"                       
#> [14] "RPPA"                                      
#> [15] "Before remove germline cnv"                
#> [16] "Gene Expression Subtype"                   
#> [17] "RABIT Use Agilent 244K Microarray"         
#> [18] "RABIT Use Affymetrix U133A Microarray"     
#> [19] "Platform-corrected PANCAN12 dataset"       
#> [20] NA                                          
#> [21] "IlluminaGA RNASeq"                         
#> [22] "RABIT Use IlluminaHiSeq RNASeqV2"          
#> [23] "RABIT Use IlluminaHiSeq RNASeq"            
#> [24] "MethylMix"                                 
#> [25] "IlluminaGA RNASeqV2"                       
#> [26] "broad automated"                           
#> [27] "wustl automated"                           
#> [28] "RABIT Use IlluminaGA RNASeqV2"             
#> [29] "RABIT Use IlluminaGA RNASeq"               
#> [30] "Batch effects normalized"                  
#> [31] "MC3 Public Version"                        
#> [32] "TCGA Sample Type and Primary Disease"      
#> [33] "RPPA pancan normalized"                    
#> [34] "Tumor copy number"                         
#> [35] "Genome-wide DNA Damage Footprint HRD Score"
#> [36] "TCGA Molecular Subtype"                    
#> [37] "iCluster cluster assignments"              
#> [38] "iCluster latent variables"                 
#> [39] "RNA based StemnessScore"                   
#> [40] "DNA methylation based StemnessScore"       
#> [41] "Pancan Gene Programs"                      
#> [42] "Immune Model Based Subtype"                
#> [43] "Immune Signature Scores"                   
#> 
# }
```
