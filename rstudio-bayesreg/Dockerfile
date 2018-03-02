####### Dockerfile #######
FROM derekpowell/rstudio-init:latest

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update -qq && apt-get -y --no-install-recommends install \
    libxt-dev \
&& install2.r --error \
    bayesboot \ 
    broom \
    fitdistrplus \
    rms \
    viridis \
    BayesFactor \
    boot \
    brms \
    fitdistrplus \
    ggmcmc \
    lme4 \
    rstanarm \
&& installGithub.r \
    mjskay/tidybayes@1432704feef258e068fb4c8304089f2d8f67cf7f \
    rmcelreath/rethinking@1.59