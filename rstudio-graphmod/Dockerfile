####### Dockerfile #######
FROM derekpowell/rstudio-bayesreg:latest

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get -y --no-install-recommends install \
	libudunits2-dev \  
&& R --no-restore --no-save -e \
	'BiocInstaller::biocLite(c("graph","Rgraphviz","RGBL"))' \
&& install2.r --error \
	BDgraph \
	bnlearn \
	bnstruct \
	geomnet \
	ggnetwork \
	ggraph \
	ggrepel \
	lavaan \
	semPlot \
	simsem \
	tidygraph \
&& installGithub.r \
	hadley/multidplyr@0085ded4048d7fbe5079616c40640dbf5982faf2