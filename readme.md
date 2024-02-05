## Background and aims ##

This project aims to take a look at the TMS data from Holmes et al., 2023, in
order to use it as the basis for simulating similar datasets and running power 
analyses. https://doi.org/10.1152/jn.00369.2023

The basic idea is to take a look at the data, model it with some Bayesian 
multi-level models, then simulate 1000s of similar datasets and summarise the 
model estimates to get a sense of the likely statistical power or precision that
future similar experiments may be expected to achieve, on average.

Most of the content is inspired by two people:

    Lisa DeBruine and her amazing {faux} R package: https://debruine.github.io/faux/

    The mighty Solomon Kurz and his Bayesian "power" blog post: 
    https://solomonkurz.netlify.app/blog/bayesian-power-analysis-part-i/
    
## Contents ##

### files ###

1) exp2a.Rproj

This is the R project file. It is called exp2a to reflect that this project is a
short demonstration of how you might calculate statistical power via data simulation
based on Experiment 2a in Holmes et al., 2023. 

2) wrangle.Rmd

This file takes the raw data Exp2a in Holmes et al., 2023 and wrangles it to 
produces plots and descriptive statistics and also re-shape it ready for modelling.

3) model.Rmd

This file takes the processed data and builds some Bayesian multi-level regression
models.

4) effects.Rmd

This file takes the model object output from step (3) and visualises the parameter
estimates.

5) sims.Rmd

This is the main simulation file. It runs through a bunch of simulations and 
shows how you can fit regression models using brms and calculate "power" and
precision of estimates for a range of target sample sizes and effect sizes. 

6) renv.lock file (and /renv/ folder)

This file and the associated folder are used with the package management software 
renv(). Once you download the project locally, renv() should automatically 
kick-in and make things happen with appropriate package versions.

### folders ###

The following folders should be self-explanatory:

*/data/*
*/figures/*
*/models/*
*/tables/*

Within these folders, a subfolder called */sims/* denotes that the material is 
from the data simulations rather than the raw data from the orgininal experiment.

