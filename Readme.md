This repository contains all the code needed to replicate the results reported in the paper corresponding to The Beauty Survey. All statistical tests were conducted in R and corresponding files can be found in the "R" folder.


All the figures were generated using python and the required scripts can be found in the folder named "python". The file "mainPaperFigures.ipynb'' contains the code needed to generate all the figures, in the order in which they appear in the paper. Multiple helper CSVs were generated while analyzing the data. These should be created automatically upon launching the notebook. If they already exist, they will not be created again. In case there are missing files however, please run the "createHelperFiles.py '' file to generate all the necessary CSVs.


Note: Many of the R tests also use the helper CSV files. Please ensure these are generated before running the tests in R.


# Data Availability


The data collected during the survey is currently available only to reviewers and can be found in the supplementary material submitted with the manuscript. Extract these files from the zipped file attached in the supplementary material and place them in the “csv_storage” folder prior to running the tests and generating the figures.


# Pre-computed Models in R


Along with the CSV files, all the statistical models generated have also been made available for ease of use. These are placed in "csv_storage/models". In case you wish to re-run these models, all the code is available in the R scripts. Please remember to set the flags to the appropriate values to generate the model files.


# Running Tests in R


Unlike the figure generation code in python, the R tests are split into multiple subfiles. Below is a short description of the tests available in each file:


- mainPaperTests.Rmd: All the statistical tests run on the centralized scores.
- runModelComparision.Rmd: This file contains the code to generate all the linear models that were created along with the other variants of models that were tested.
- mainPaperTests_fullData.Rmd: This file contains all the tests run using the per-rater scores. This file mainly generates the results of the estimated marginal means. These are already pre-computed and made available in the "csv_storage" folder.
-computeNewSpacing_OSM.Rmd: This file contains the code needed to re-run the OSM's and compute the new scales.


# Questions


While extreme care has been taken to ensure all the necessary data and code is available in this repository, errors do tend to creep in. In case something does not work well, please raise an issue on the repository or feel free to reach out to me at aditya@ellisalicante.org.

