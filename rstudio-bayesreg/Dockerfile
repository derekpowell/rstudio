####### Dockerfile #######
FROM derekpowell/rstudio-init:latest

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update -qq && apt-get -y --no-install-recommends install \
    libxt-dev \
&& install2.r --error \
    --deps TRUE \
    BayesFactor \
    boot \
    brms \
    ggmcmc \
    lme4 \
    rstanarm \
    fitdistrplus \
&& install2.r --error \
	--deps NA \
	broom \
	bayesboot \	
	rms \
	viridis \
&& R --no-restore --no-save -e 'devtools::install_github("mjskay/tidybayes")' \
&& R --no-restore --no-save -e 'devtools::install_github("rmcelreath/rethinking")'