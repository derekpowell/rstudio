####### Dockerfile #######
FROM derekpowell/rstudio-init:latest

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update -qq && apt-get -y --no-install-recommends install \
    libxt-dev \
&& install2.r --error --skipinstalled \
    bayesboot \
    # broom \
    fitdistrplus \
    # rms \
    # viridis \
    BayesFactor \
    boot \
    brms \
    ggmcmc \
    lme4 \
    # rstanarm \
    tidybayes \
	ggrepel \
&& installGithub.r \
    rmcelreath/rethinking@1.59
