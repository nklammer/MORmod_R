# MORmod_R
Version control of my thesis work in R

# R integration
There is an option(?) to run shell commands via engines like `bash` from inside an R markdown `.Rmd` document. `knitr` [supports](https://bookdown.org/yihui/rmarkdown-cookbook/eng-bash.html#eng-bash) `bash` language command chunks on Unix and macOS. It is not impossible for Windows users to [run Shell scripts](https://yihui.org/knitr/options/?version=1.2.5042&mode=desktop#language-engines), but you will have to install additional software (such as Cygwin or the Linux Subsystem).

Currently, `bash is not recognized as an internal or external command, operable program or batch file.`

### `algorithm_compare`
Add in table comparison of cluster member groupings across cluster methods.

Returns output of Figure PNG that is a panelized figure of 6 clusters across 52 weeks to illustrate the similarities between energy use profiles.

Includes outputs of `algorithm_compare_k13.csv` and `algorithm_compare_k13.xlsx` that compares different clustering algorithms for the objective to create 13 clusters.

Uses R data from the `hvac_dhw_var.Rda` case for illustrative purposes.

### `input/*`
This is where I manually situated the output variable data that was output from the `.eso` files. R analysis read in data points to this directory.

### `downsampling`
In this folder, I control for temporal period using downsampling and examine its effect on the meteric CV-RMSE and NMBE.

### `images`
In this directory I placed bitmap images that were produced by R but are meant to be anchored into `knitr` HTML notebooks. This was for various reasons.

### `sensitivity_analysis`
Update for table in Results chapter.

#### `Calcs.xlsx`
This file is important but slightly misplaced. Sheet tab "WindProfile" shows the calculation to neglect wind-height effects in simulation. Sheet tab "CurveCubic" visualizes the part load efficiency curve for a cooling coil to prove out that equipment sizing does indeed matter in granular models.

#### `Cluster_test.Rmd`
Sketch notebook that practiced the manipulation of R packages `cluster` and `pvclust`. Adapted from code written by Gregor Henze.

#### `ILAS.Rda`

#### `IdLoAiSy-Map.csv`
Simple two column table that maps the Zone string ID (e.g., "0_BDRM_1_2") to the Ideal Air Loads System Number. The Ideal...Number was assigned as the `EnableIdealAirLoads` measure was affected. I believe (?) this may be deprecated now that I have changed the `#run` method of the measure to include the human-readable string name of the zone in the name of the Ideal Air Load System.

#### `Multifamily_Parameters.xlsx`
Another important, misplaced spreadsheet. This is a master table is a quick reference for finding model geometry parameters quickly given the zone name (e.g., space type, floor multiplier, space area m2, zone volume m3, above ground gross ext wall area m2...).

#### `ZoneFloorArea-Map.csv`
Simple two column table that maps the Zone string ID (e.g., "0_BDRM_1_2") to its floor area (m2). Necessary for parameter normalization before clustering action.

#### `hvac_dhw_novar.Rda`

#### `hvac_dhw_novar_red.Rda`

#### `hvac_dhw_var.Rda`

#### `ilas_dhw_novar.Rda`

#### `ilas_dhw_novar_red.Rda`

#### `ilas_no_dhw_red.Rda`

#### `ilas_nodhw.Rda`

#### `multi_smooth_ilas_nodhw.png`

#### `step0.1_pre-process_ilas_nodhw.Rmd`

#### `step0.2_pre-process_ilas_dhw_novar.Rmd`

#### `step0.3_pre-process_hvac_dhw_novar.Rmd`

#### `step0.4_pre-process_hvac_dhw_var.Rmd`

#### `step10_final_results.Rmd`

#### `step1_join_epw.Rmd`

#### `step2.1_cluster_model.Rmd`

#### `step2.2_cluster_model.Rmd`

#### `step2.3_cluster_model.Rmd`

#### `step2.4_cluster_model.Rmd`

#### `step4_cluster_viz.Rmd`

#### `step5_affinity_prop.Rmd`