# Structure_Clumpp_Spatial_inference_R
Rmarkdown scripts and test files for running STRUCTURE analysis, combining replicates with CLUMPP, and generating assignment barplots and spatial interpolation of ancestry coefficient. The map of spatial interpolation of ancestry is similar to those generated by TESS, but the geographic information is not used by STRUCTURE to infer population ancenstry.

The applications for STRUCTURE and CLUMP need to be installed on your system in the default path for R to run them.

The last step, mapping spatial interpolation of ancestry, uses the same method as implemented in TESS, but I've only tested it briefly,  and it appears to be only mapping based on assignment probabilities >0.5, so there may be something about the converted Qplot that is different between TESS and STRUCTURE. In principle, it should work, but still needs debugging. It is also modified to map to marine instead of terrestrial data (see notes in the script), and the map is focused on the anti-meridian (the central Pacific). The tutorial for TESS (https://github.com/bcm-uga/TESS3_encho_sen/blob/master/vignettes/main-vignette.Rmd) provides instructions for mapping to land, and if the data do not cross the anti-meridian. 

Contents:

1 load library

2 load genotype data and stratification schemes

3 Map the data points

4 Structure analysis

5 get map information and set up map structure

6 Run clumpp on structure iterations, plot barplots and map spatial interpolation of ancestry coefficient from STRUCTURE
