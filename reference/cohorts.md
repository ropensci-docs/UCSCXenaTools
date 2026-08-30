# Get cohorts of XenaHub object

Get cohorts of XenaHub object

## Usage

``` r
cohorts(x)
```

## Arguments

- x:

  a
  [XenaHub](https://docs.ropensci.org/UCSCXenaTools/reference/XenaHub.md)
  object

## Value

a character vector contains cohorts

## Examples

``` r
xe = XenaGenerate(subset = XenaHostNames == "tcgaHub"); cohorts(xe)
#>  [1] "TCGA Ovarian Cancer (OV)"                                   
#>  [2] "TCGA Kidney Clear Cell Carcinoma (KIRC)"                    
#>  [3] "TCGA Lower Grade Glioma (LGG)"                              
#>  [4] "TCGA Kidney Papillary Cell Carcinoma (KIRP)"                
#>  [5] "TCGA Pan-Cancer (PANCAN)"                                   
#>  [6] "TCGA Bile Duct Cancer (CHOL)"                               
#>  [7] "TCGA Colon and Rectal Cancer (COADREAD)"                    
#>  [8] "TCGA Adrenocortical Cancer (ACC)"                           
#>  [9] "TCGA Cervical Cancer (CESC)"                                
#> [10] "TCGA Rectal Cancer (READ)"                                  
#> [11] "TCGA Sarcoma (SARC)"                                        
#> [12] "TCGA Large B-cell Lymphoma (DLBC)"                          
#> [13] "TCGA Prostate Cancer (PRAD)"                                
#> [14] "TCGA Lung Cancer (LUNG)"                                    
#> [15] "TCGA Liver Cancer (LIHC)"                                   
#> [16] "TCGA Kidney Chromophobe (KICH)"                             
#> [17] "TCGA Head and Neck Cancer (HNSC)"                           
#> [18] "TCGA Pheochromocytoma & Paraganglioma (PCPG)"               
#> [19] "TCGA Esophageal Cancer (ESCA)"                              
#> [20] "TCGA Thyroid Cancer (THCA)"                                 
#> [21] "TCGA Lung Adenocarcinoma (LUAD)"                            
#> [22] "TCGA Acute Myeloid Leukemia (LAML)"                         
#> [23] "TCGA Bladder Cancer (BLCA)"                                 
#> [24] "TCGA Melanoma (SKCM)"                                       
#> [25] "TCGA Lung Squamous Cell Carcinoma (LUSC)"                   
#> [26] "TCGA Testicular Cancer (TGCT)"                              
#> [27] "TCGA Pancreatic Cancer (PAAD)"                              
#> [28] "TCGA Glioblastoma (GBM)"                                    
#> [29] "TCGA Stomach Cancer (STAD)"                                 
#> [30] "TCGA Mesothelioma (MESO)"                                   
#> [31] "TCGA Ocular melanomas (UVM)"                                
#> [32] "TCGA lower grade glioma and glioblastoma (GBMLGG)"          
#> [33] "TCGA Thymoma (THYM)"                                        
#> [34] "TCGA Endometrioid Cancer (UCEC)"                            
#> [35] "TCGA Breast Cancer (BRCA)"                                  
#> [36] "TCGA Uterine Carcinosarcoma (UCS)"                          
#> [37] "TCGA Colon Cancer (COAD)"                                   
#> [38] "TCGA Formalin Fixed Paraffin-Embedded Pilot Phase II (FPPP)"
```
