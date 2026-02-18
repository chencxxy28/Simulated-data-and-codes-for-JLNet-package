**JLNet** is a novel analytical framework integrating multiple statistical and machine learning techniques, including propensity score weighting, projection methods, regularized regression, and unsupervised learning. It offers several unique features not available in existing toolkits, including the flexible identification of high-dimensional patient-level factors associated with care outcomes (potentially with time-varying effects), the computationally efficient detection of latent hospital clusters, and the ability to handle real-world data complexities, such as patient dropout and non-normally distributed outcomes. 


# Installation

``` r
if (!require("devtools")) {
  install.packages("devtools")
}
devtools::install_github("yilinzhang066/JLNet")
```


After installing the *JLNet* package, the simulated data *simdata* can be loaded and viewed using the code:
``` r
library(JLNet)
set.seed(12345)
data("simdata", package = "JLNet")
head(simdata)

     id   hosp visit   subj_x_1    subj_x_2  subj_x_3 
1 10001    1     1     7.779783        1     4.918035
2 10001    1     2     7.603686        1     4.918035
3 10001    1     3     7.700258        1     4.918035
4 10001    1     4     7.474295        1     4.918035
5 10001    1     5     7.912472        1     4.918035
6 10001    1     6     6.660966        1     4.918035
```

In this simulated pseudo data, we considered a setting with many patient-level variables, each having a fixed effect on the outcome. Specifically, we generated a dataset comprising 200 hospitals and around 5, 000 patients, where the simulated dataset included 205 patient-level variables-of which 5 were predictive, while the remaining 200 were redundant. Longitudinal outcomes were generated based on a skewed distribution, with in total six observations per subject, though some patients had fewer observations due to dropout, leading to an approximately 20% patient-level missingness rate

Our team has developed a R package for implementing our methods. We refer interested readers to following webiste for more detailed JLNet package description, detailed functions, and tutorial managed by our team (still updating the package this package in recent days by adding more functions):
https://github.com/yilinzhang066/JLNet

