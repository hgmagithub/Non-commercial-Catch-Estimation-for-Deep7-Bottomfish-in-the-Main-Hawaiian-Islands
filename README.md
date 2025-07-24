# Non-commercial Catch Estimation for Deep7 Bottomfish in the Main Hawaiian Islands

## Overview
Survey data and catch estimates in 2003–2022 from the Hawaii Marine Recreational Fishing Survey (HMRFS) were evaluated to obtain non-commercial catch weight estimates for the main Hawaiian Islands Deep7 bottomfish complex. The current HMRFS estimates do not distinguish between catch to be sold vs. catch not for sale from expense fishers (who sometimes sell fish to cover fishing expenses) or part-time commercial fishers. Fishers selling the catch are required to report the number of fish and weight landed in a commercial reporting system. To provide a non-commercial catch estimate (product of catch rate and fishing effort), catch claimed as unsold in HMRFS was used for catch rate estimation. The catch rate estimates were smoothed by a Kalman filter to reduce unrealistically large fluctuations in annual catch estimates. Fishing effort estimates from a previous telephone survey were adjusted to make the effort estimates similar to the current mail survey for fishing effort. The non-commercial catch estimates from this study have been used in combination with the reported catch from the mandatory commercial fishing reports to obtain total fish removal for the Deep7 bottomfish benchmark stock assessment in 2024.

## R scripts and data files
Thescript in the "R Scripts" folder can estimate total catch in HMRFS. The total catch estimates can be compared (and validated) with the estimates (including variance) queried from the NOAA Fisheries Marine Recreational Information Program (https://www.fisheries.noaa.gov/data-tools/recreational-fisheries-statistics-queries). The proportion of non-sold catch was also estimated with the R script (for total catch) to compare with the proportion estimates from Ma et al. 2019. When "catch_type" is set as "Non-sold catch', the catch with dispostion "sold/to be sold" is not read into R and the catch estimation is for unsold catch only. 

The "meanweight" file in the "Data" folder include the mean weights for seven bottomfish species based on the mean of measured and lenghth-drived weights during 2003-2022. The "Mutiplier" are for the calibration of fishing effort estimates from the previous Coastal Household Telephone Survey (2003-2017) to make these effort estimates comparable with the estimates from the current Fishing Effort Survey (mail survey).
## Installing
Three R packages need to be installed to read SAS data files ("sas7bdat') and to smooth time-series data with Kalman Filter and Smoother ("KFAS") or moving average ("zoo").

## Resources
Ma, H., and Ogawa, T. (2016). Hawaii Marine Recreational Fishing Survey: A Summary of Current Sampling, Estimation, and Data Analyses. NOAA Tech. Memo., NOAA-TM-NMFS-PIFSC-55, 43 p. http://dx.doi.org/10.7289/V5/TM-PIFSC-55

Ma, H., Matthews, T., Syslo, J., Ducharme-Barth, N. 2023. Non-commercial Catch Estimation for Deep7 Bottomfish in the Main Hawaiian Islands. In: Joint Statistical Meetings 2023. Toronto, Canada. https://doi.org/10.5281/zenodo.8388018.

Syslo J., Oshima M., Ma H., Ducharme-Barth N., Nadon M., Carvalho, F. (2024). Benchmark stock assessment for the main Hawaiian Islands Deep 7 bottomfish complex in 2024 with catch projections through 2029. Department of Commerce. NOAA Stock Assessment Report. NMFS-PIFSC-157. doi:10.25923/5ssg-8d54
## Version Control Platform
- Git

## License
See the [LICENSE.md](./LICENSE.md) for details

## Disclaimer
This repository is a scientific product and is not official communication of the National Oceanic and Atmospheric Administration, or the United States Department of Commerce. All NOAA GitHub project code is provided on an ‘as is’ basis and the user assumes responsibility for its use. Any claims against the Department of Commerce or Department of Commerce bureaus stemming from the use of this GitHub project will be governed by all applicable Federal law. Any reference to specific commercial products, processes, or services by service mark, trademark, manufacturer, or otherwise, does not constitute or imply their endorsement, recommendation or favoring by the Department of Commerce. The Department of Commerce seal and logo, or the seal and logo of a DOC bureau, shall not be used in any manner to imply endorsement of any commercial product or activity by DOC or the United States Government.
