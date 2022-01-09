
<!-- README.md is generated from README.Rmd. -->

# <img src="figures/taxmatch.PNG" align="right" height="230"/> Matching (phytoplankton imagery) categories to Worms accepted name

<!-- badges: start -->

[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](https://opensource.org/licenses/MIT) [![R 4.1.1](https://img.shields.io/badge/R-4.1.1-red.svg)](https://www.r-project.org/)

<!-- badges: end -->

## Tutorial 

This repository contains a tutorial to match categories, especially categories from imagery, to accepted taxonomic names from WoRMS: <https://virginiesonnet.github.io/TaxonomyMatch/>. Although designed for imagery with sections specific to morphological, non-plankton and temporary categories, the section for taxonomical categories is extensive and **can be used for any list of marine organisms**. 

It tries to incorporate some of the guidelines presented in Neeley et al. (2021) to facilitate submission to databases such as SeaBASS or EDI. 

*Neeley, A., S. Beaulieu, C. Proctor, I. Cetinić, J. Futrelle, I. Soto Ramos, H. Sosik et al. "Standards and practices for reporting plankton and other particle observations from images. Technical Manual." (2021).*


## Overview 

The different steps include: 

1. Trimming and cleaning the names 
2. Resolving the taxonomic names: exact match in Worms, duplicates, accepted name, fuzzy match, record not in Worms but in AlgaeBase 
3. Resolving categories linked to morphology
4. Resolving categories non-plankton with the Phytoplankton Taxonomy Working Group namespace
5. Assigning temporary categories to the Eukaryota ID of AlgaeBase 
6. Combining into a dataset with the original name, accepted name (scientificName), scientificNameID (lsid based on the AphiaID from Worms), kingdom and rank



## Files 

The Rmd version of the tutorial is available in the ***scripts*** folder: *taxonomy_matchup.Rmd*. It uses `tidyverse` (Wickham et al., 2019) structure and mostly builds on the packages `worrms` (Chamberlain, 2020) and `taxize` (Chamberlain and Szoecs, 2013) with a couple of functions from `taxonomyCleanr` (Smith, 2021) and `algaeClassify` (Patil et al., 2019). 

The example csv file used as input is included in the ***data*** folder (*example_taxo.csv*) as well as the output file (*matched_example_taxo.csv*).


## Contact 

In case you spot something that can be improved or just found the script useful, don't hesitate to send me a message at *virginie_sonnet@uri.edu*! 
