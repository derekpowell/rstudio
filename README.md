# RStudio Docker Images

A single repository for all my RStudio docker image layers, to be automatically built on docker cloud. I plan for these images to form a linear stack.

## rstudio-init

This draws on the most-recently versioned Rocker/tidyverse image (3.4.3 as of March 1, 2018). This is a base image where I add scripts to the image `\init`, primarily to add customizations and improve workflow.

## rstudio-bayesreg

This image adds a collection of packages for Bayesian regression and multilevel modeling. The basis for most of these tools is the probabilistic programming language [Stan](http://mc-stan.org/).

It features:

* Bayesian multi-level regression: with [brms](https://github.com/paul-buerkner/brms) and [rstanarm](http://mc-stan.org/users/interfaces/rstanarm)
* Bayesian hypothesis testing: with [BayesFactor](http://bayesfactorpcl.r-forge.r-project.org/)
* Distributional modeling in Stan with the [rethinking](https://github.com/rmcelreath/rethinking) package
* Bootstrapping tools: [boot](https://cran.r-project.org/web/packages/boot/boot.pdf) and [bayesboot](https://github.com/rasmusab/bayesboot)
* Modeling and plotting tools: [broom](https://github.com/tidyverse/broom), [tidybayes](https://github.com/mjskay/tidybayes), and [ggmcmc](https://github.com/xfim/ggmcmc)
* Non-bayesian regression tools: [lme4](https://github.com/lme4/lme4) and [rms](https://www.r-bloggers.com/introduction-to-the-rms-package/)
* Misc.: fitdistrplus, viridis, ggthemes

## rstudio-graphmod

_Future project_: Adds graphical modeling tools: bnlearn, BDgraph, bnstruct, RgraphViz, graph, RBGL, lavaan, simsem, tidygraph, ggraph, ggnetwork, geomnet, semPlot, corrplot(?)