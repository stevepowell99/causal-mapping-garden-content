---
date: 2025-04-09
---

# Open-source causal mapping functions

An earlier version app CausalMap3. The app itself is free to use for analysing existing causal mapping data files but it is closed source, so the functions are a reproducible window into the algorithms and can be used by anyone who wants to analyse and visualise causal mapping data without using the Causal Map app.

When we get a chance, we will release them as a full R package.  But for now you can read and download a single [R script](https://www.dropbox.com/scl/fi/mtlaf5rmmdrgp3bxbrydz/cm3functions.R?rlkey=7hli0uaookisr9seahpzczynk&dl=0) which contains the functions and all you need to use them.

We are still in the process of documenting the functions. To make them easier to use, we have a  [vignette](https://www.dropbox.com/scl/fi/l6d3pamox47it9xphqmyr/examples.rmd?rlkey=o5v19ra7xirh91kb8uc38uvbh&dl=0) which demonstrates the use of many of the functions as applied to example causal mapping data files (here is the [main example file](https://www.dropbox.com/scl/fi/ulrtbj9fmgu1ltdamsvhy/example-file.xlsx?rlkey=pczexdevcxgz4if2muqwr0dng&dl=0) and here is a [special example to demonstrate the use of combined opposites](https://www.dropbox.com/scl/fi/t9fnja78jo2zb650fesqs/opposites-example.xlsx?rlkey=t9cd4afr77te3bs98hnv6rm5v&dl=0)).

The vignette is an .Rmd file: if you process it using the package *knitr* or by pressing *Knit* in Rstudio, you should get output like [this](https://www.pogol.net/Public/examples.html). It contains over 50 different types of map.