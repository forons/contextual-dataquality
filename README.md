# Contextual Data-Quality Framework

This is the repository containing the notions for performing an analysis about the contextual data quality of a dataset.

Hence, in this repository, we showcase the usage of the framework through some bash scripts, which actually perform the following steps.

## Noise Generation
The first part of the process involves the generation of the noise in the dataset.

The source code for the noise generation can be found [here](https://github.com/forons/noise-generator).

## Task Run
Then, we run over the given dataset and over the set of noisy instances of the dataset the chosen task.

## Distance Measurement
Finally, we measure the distance in the results from the original dataset of each of the noisy instances generated from it.
The source code for the distance measurement can be found [here](https://github.com/forons/distance-measurement).

## Sensitivity Factors
After having performed the distance measurement, we collect the results about a single noise with all the percentages run for it. This set of elements allows us to compute the sensitivity factors about a noise, which present an analysis of the impact of such noise on the results of the task performed.

The sensitivity factors that we implemented consider a linear relationship (linear regression with LLS) and a polynomial correlation between the noise percentage introduced and the distance of the results. Then, we measure also the Spearman correlation to check if they follow the same behaviour of not.