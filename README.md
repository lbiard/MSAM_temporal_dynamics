# MSAM_temporal_dynamics

This repository hosts data and R code to reproduce the Multi-Species Abundance Model (MSAM) from García-Navas V., Bliard L., Ozgul A. (2024). Impact of a ‘reverse keystone species’ on the temporal dynamics of bird communities in Australia. Biological Conservation. https://doi.org/10.1016/j.biocon.2024.110698  


## GENERAL INFORMATION

1. Title: "Data and code to reproduce the Multi-Species Abundance Model (MSAM) from: Impact of a ‘reverse keystone species’ on the temporal dynamics of bird communities in Australia"

2. Author information (for the Multi Species Abundance Model):
       
       Name: Louis Bliard
		   Institution: University of Zurich
		   Email: louis.bliard@evobio.eu

   3. Date of data collection (single date, range, approximate date): 1998-2020

4. Geographic location of data collection: south-east Queensland

5. Information about funding sources that supported the collection of the data: NA


## SHARING/ACCESS INFORMATION

1. Licenses/restrictions placed on the data:

2. Links to publications that cite or use the data: García-Navas V, Bliard L, Ozgul A. 2024. Impact of a ‘reverse keystone species’ on the temporal dynamics of bird communities in Australia. Biological Conservation. https://doi.org/10.1016/j.biocon.2024.110698 

3. Links to other publicly accessible locations of the data: NA

4. Links/relationships to ancillary data sets: NA

5. Was data derived from another source? yes
	A. If yes, list source(s): Australian Bird Atlas https://birdata.birdlife.org.au


## METHODOLOGICAL INFORMATION

1. Methods for processing the data: All data were processed in R.

2. Software-specific information needed to interpret the data:
R statistical software, version 4.1.2. 
JAGS https://mcmc-jags.sourceforge.io/


## DATA & FILE OVERVIEW

1. File List: 

- `data.RData` R data object containing the bird surveys data needed to run the MSAM model. The output of the model is not included because the file is too large for storage on github.

- `msam_longitudinal_model.R` Code containing the JAGS model to run the MSAM analysis, which is used to compute estimated true abundance for species at different sites.

2. Relationship between files, if important: 
The RData file "data.RData" is needed to run the MSAM analysis with the "msam_longitudinal_model" file. 


### DATA-SPECIFIC INFORMATION FOR: `data.RData`

1. Number of variables: NA

2. Number of cases/rows: NA

3. Object List: 
- f1: vector of length 69 containing the season of first survey for each site.
- f2: vector of length 69 containing the season of last survey for each site.
- season_vec: vector of length 22 corresponding to each season (starting from season 1998/1999).
- site_vec: vector of length 69 corresponding to each site name.
- species_vec: vector of length 159 corresponding to each species name.
- y: raw occurence data. 4 dimensional array of dimensions 69 (number of sites) * 7 (number of repeated surveys) * 22 (number of seasons) * 159 (number of species).

4. Missing data codes: NA

5. Specialized formats or other abbreviations used: NA
