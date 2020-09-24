# HPAStain.R

HPAStain.R is an [R package](https://github.com/tnieuwe/HPAStainR)/[Shiny app](https://32tim32.shinyapps.io/HPAStainR/) used to query the Human Protein Atlas for staining data. The purpose of this tool is to test if a list of proteins/genes is associated with a certain cell type in a HPA tested tissue. E.g. you have a list of protein coding genes from a differential expression single cell analysis and want to see if these proteins are associated with a known cell type. Instead of querying HPA multiple times you can load your list in HPAStainR which will return a ranked table of the cell types with the most protein staining.

The package has officially been accepted at Bioconductor, and package deveopment still continues at https://github.com/tnieuwe/HPAStainR, there will be no further updates to the HPAStainR package here, this github exists to now host the experiment used in the HPAStainR paper.

I am keeping this repository as I believe the README is a useful supplement and this repository holds the data that will be submitted hopefully as a paper.

This is my first time developing a package on Github, any and all feedback is appreciated!

## Getting Started

HPAStainR in its current form is a online Shiny app and R package. The package will soon be available on Bioconductor,  until then feel free to install it using `devtools` from its current repository up to date repository https://github.com/tnieuwe/HPAStainR.

Run the below R code to install the package using the `devtools` library.

`devtools::install_github('32tim32/stainR/package_HPAstainR')`
(stainR was the previous name)

Another way to use it is go to my shiny app website posted here and above:
https://32tim32.shinyapps.io/HPAStainR/ 

There is also a brief [vignette](https://htmlpreview.github.io/?https://github.com/tnieuwe/HPAstainR_dev_paper/blob/master/HPAStainR.html) to get you started with the package as well.

### Prerequisites

Depends: `dplyr` and `tidyr`
Imports: `utils`, `stats`, `scales`, `stringr`, `tible`, and `shiny`
Suggests: `knitr`, `qpdf`, `testhat`
The datasets required are below, but HPAStainR package has a function, `HPA_data_downloader()` that can download them for you either permanently or temporarily (via the `save_file` argument):

Normal Tissue: https://www.proteinatlas.org/download/normal_tissue.tsv.zip

Cancer Tissue: https://www.proteinatlas.org/download/pathology.tsv.zip

*Note*: these are large files but required to run HPAStainR, HPAStainR also has built in functions to do this.

## Files for Paper Analysis

* *HPAStainR_paper_analysis.rmd:* The Rmarkdown file which includes all the analyses completed for the HPAStainR paper including:
  * All figures
  * All CSVs
  * PanglaoDB specific analyses
  * Recapitulation of [McCall et. al](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5011060/) results
* *HPAStainR_paper_analysis.html:* The html printout of the Rmarkdown file.
* *data_out:* Where the output of the figures and CSVs from HPAStainR_paper_analysis.rmd go.

### Other folders

* *old_versions*: Holds previous package versions and analyses
* *old vignette*: Holds previous vignettes, most up to date vignette is in the Bioconductor version
* *old_files*: General old outputs that are no longer relevant to the main paper

## Built With

* [dplyr](https://dplyr.tidyverse.org/) - Data.frame manipulation
* [tidyr](https://tidyr.tidyverse.org/) - For creating tidy data
* [Shiny](https://shiny.rstudio.com/) - For the shinyapp UI
* [stringr](https://stringr.tidyverse.org/) - String manipulation
* [tibble](https://tibble.tidyverse.org/) - For data.frame replacements
* [Scales](https://www.rdocumentation.org/packages/scales/versions/0.4.1) - Generating percents

## Authors

* **Tim Nieuwenhuis** - *Concept and Coder* - [tnieuwe](https://github.com/tnieuwe/)
* **Marc Halushka** - *Mentor* - [mhalushka](https://github.com/mhalushka)


## Acknowledgments

* Thank you Stephanie Yang and Veronica Busa for helpful comments - [syang93](https://github.com/syyang93/) & [vbusa1](https://github.com/vbusa1)
* Thank you Matt McCall and Zach Brehm for reviewing the code - [mccallm](https://github.com/mccallm) & [zachbrehm](https://github.com/zachbrehm)
* Human Protein Atlas for data availability and data structure
* PurpleBooth for the README template - [PurpleBooth](https://gist.github.com/PurpleBooth/)
* The people at Bioconductor for reviewing my tool

# License and DOI
Artistic-2.0

https://zenodo.org/badge/246627856.svg
