####### Dockerfile #######
FROM derekpowell/rstudio-bayesreg:latest

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get -y --no-install-recommends install \
	libudunits2-dev \
	jags \
&& R --no-restore --no-save -e \
	'BiocInstaller::biocLite(c("graph","Rgraphviz","RBGL"))' \
&& install2.r --error --skipinstalled \
	# BDgraph \
	bnlearn \
	# bnstruct \
	# geomnet \
	# ggnetwork \
	ggraph \
	ggrepel \
	lavaan \
	semPlot \
	simsem \
	# tidygraph \
	# gRain \
	# gRim \
	HydeNet \
	# blavaan \
&& installGithub.r \
	hadley/multidplyr@0085ded4048d7fbe5079616c40640dbf5982faf2
