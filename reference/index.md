# Package index

## Standard dataset query and download pipeline

Select, query, download and load datasets.

- [`XenaData`](https://docs.ropensci.org/UCSCXenaTools/reference/XenaData.md)
  : Xena Hub Information
- [`XenaScan()`](https://docs.ropensci.org/UCSCXenaTools/reference/XenaScan.md)
  : Scan all rows according to user input by a regular expression
- [`XenaGenerate()`](https://docs.ropensci.org/UCSCXenaTools/reference/XenaGenerate.md)
  : Generate and Subset a XenaHub Object from 'XenaData'
- [`XenaFilter()`](https://docs.ropensci.org/UCSCXenaTools/reference/XenaFilter.md)
  : Filter a XenaHub Object
- [`XenaBrowse()`](https://docs.ropensci.org/UCSCXenaTools/reference/XenaBrowse.md)
  : View Info of Dataset or Cohort at UCSC Xena Website Using Web
  browser
- [`XenaQuery()`](https://docs.ropensci.org/UCSCXenaTools/reference/XenaQuery.md)
  : Query URL of Datasets before Downloading
- [`XenaDownload()`](https://docs.ropensci.org/UCSCXenaTools/reference/XenaDownload.md)
  : Download Datasets from UCSC Xena Hubs
- [`XenaPrepare()`](https://docs.ropensci.org/UCSCXenaTools/reference/XenaPrepare.md)
  : Prepare (Load) Downloaded Datasets to R

## Download a subset of dataset

Download a subset of dataset for target analysis.

- [`fetch()`](https://docs.ropensci.org/UCSCXenaTools/reference/fetch.md)
  [`fetch_dense_values()`](https://docs.ropensci.org/UCSCXenaTools/reference/fetch.md)
  [`fetch_sparse_values()`](https://docs.ropensci.org/UCSCXenaTools/reference/fetch.md)
  [`fetch_dataset_samples()`](https://docs.ropensci.org/UCSCXenaTools/reference/fetch.md)
  [`fetch_dataset_identifiers()`](https://docs.ropensci.org/UCSCXenaTools/reference/fetch.md)
  [`has_probeMap()`](https://docs.ropensci.org/UCSCXenaTools/reference/fetch.md)
  : Fetch Data from UCSC Xena Hosts

## One-click download function

Download datasets by setting options in one function.

- [`downloadTCGA()`](https://docs.ropensci.org/UCSCXenaTools/reference/downloadTCGA.md)
  : Easily Download TCGA Data by Several Options
- [`getTCGAdata()`](https://docs.ropensci.org/UCSCXenaTools/reference/getTCGAdata.md)
  : Get TCGA Common Data Sets by Project ID and Property
- [`availTCGA()`](https://docs.ropensci.org/UCSCXenaTools/reference/availTCGA.md)
  : Get or Check TCGA Available ProjectID, DataType and FileType
- [`showTCGA()`](https://docs.ropensci.org/UCSCXenaTools/reference/showTCGA.md)
  : Show TCGA data structure by Project ID or ALL

## Utility

Useful functions.

- [`XenaDataUpdate()`](https://docs.ropensci.org/UCSCXenaTools/reference/XenaDataUpdate.md)
  : Get or Update Newest Data Information of UCSC Xena Data Hubs
- [`hosts()`](https://docs.ropensci.org/UCSCXenaTools/reference/hosts.md)
  : Get hosts of XenaHub object
- [`cohorts()`](https://docs.ropensci.org/UCSCXenaTools/reference/cohorts.md)
  : Get cohorts of XenaHub object
- [`datasets()`](https://docs.ropensci.org/UCSCXenaTools/reference/datasets.md)
  : Get datasets of XenaHub object
- [`samples()`](https://docs.ropensci.org/UCSCXenaTools/reference/samples.md)
  : Get Samples of a XenaHub object according to 'by' and 'how' action
  arguments
- [`fetch()`](https://docs.ropensci.org/UCSCXenaTools/reference/fetch.md)
  [`fetch_dense_values()`](https://docs.ropensci.org/UCSCXenaTools/reference/fetch.md)
  [`fetch_sparse_values()`](https://docs.ropensci.org/UCSCXenaTools/reference/fetch.md)
  [`fetch_dataset_samples()`](https://docs.ropensci.org/UCSCXenaTools/reference/fetch.md)
  [`fetch_dataset_identifiers()`](https://docs.ropensci.org/UCSCXenaTools/reference/fetch.md)
  [`has_probeMap()`](https://docs.ropensci.org/UCSCXenaTools/reference/fetch.md)
  : Fetch Data from UCSC Xena Hosts
- [`XenaQueryProbeMap()`](https://docs.ropensci.org/UCSCXenaTools/reference/XenaQueryProbeMap.md)
  : Query ProbeMap URL of Datasets

## Helpers

Helper functions.

- [`xena_default_hosts()`](https://docs.ropensci.org/UCSCXenaTools/reference/xena_default_hosts.md)
  : UCSC Xena Default Hosts
- [`to_snake()`](https://docs.ropensci.org/UCSCXenaTools/reference/to_snake.md)
  : Convert camel case to snake case
- [`UCSCXenaTools-dynamic`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_all_cohorts`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_all_datasets`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_all_datasets_n`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_all_field_metadata`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_cohort_samples`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_cohort_summary`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_dataset_fetch`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_dataset_field`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_dataset_field_examples`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_dataset_field_n`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_dataset_gene_probe_avg`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_dataset_gene_probes_values`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_dataset_list`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_dataset_metadata`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_dataset_probe_signature`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_dataset_probe_values`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_dataset_samples`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_dataset_samples_ndense_matrix`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_dataset_sources`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_dataset_status`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_datasets_null_rows`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_feature_list`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_field_codes`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_field_metadata`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_gene_transcripts`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_match_fields`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_probe_count`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_probemap_list`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_ref_gene_exons`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_ref_gene_position`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_ref_gene_range`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_segment_data_examples`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_segmented_data_range`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_sparse_data`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_sparse_data_examples`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_sparse_data_match_field`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_sparse_data_match_field_slow`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_sparse_data_match_partial_field`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_sparse_data_range`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.p_transcript_expression`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_all_cohorts`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_all_datasets`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_all_datasets_n`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_all_field_metadata`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_cohort_samples`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_cohort_summary`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_dataset_fetch`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_dataset_field`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_dataset_field_examples`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_dataset_field_n`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_dataset_gene_probe_avg`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_dataset_gene_probes_values`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_dataset_list`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_dataset_metadata`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_dataset_probe_signature`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_dataset_probe_values`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_dataset_samples`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_dataset_samples_ndense_matrix`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_dataset_sources`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_dataset_status`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_datasets_null_rows`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_feature_list`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_field_codes`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_field_metadata`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_gene_transcripts`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_match_fields`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_probe_count`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_probemap_list`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_ref_gene_exons`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_ref_gene_position`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_ref_gene_range`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_segment_data_examples`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_segmented_data_range`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_sparse_data`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_sparse_data_examples`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_sparse_data_match_field`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_sparse_data_match_field_slow`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_sparse_data_match_partial_field`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_sparse_data_range`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  [`.xq_transcript_expression`](https://docs.ropensci.org/UCSCXenaTools/reference/UCSCXenaTools-dynamic.md)
  : UCSC Xena Dynamic Objects

## Class

Class and related function.

- [`XenaHub-class`](https://docs.ropensci.org/UCSCXenaTools/reference/XenaHub-class.md)
  [`.XenaHub`](https://docs.ropensci.org/UCSCXenaTools/reference/XenaHub-class.md)
  : Class XenaHub
- [`XenaHub()`](https://docs.ropensci.org/UCSCXenaTools/reference/XenaHub.md)
  : Generate a XenaHub Object
