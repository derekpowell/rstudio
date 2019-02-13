####### Dockerfile #######
FROM rocker/verse:3.4.3

ENV DEBIAN_FRONTEND noninteractive

COPY set_theme.sh /etc/cont-init.d/theme

COPY git_config.sh /etc/cont-init.d/gitconfig

COPY rstudio_bindings.json /home/rstudio/.R/rstudio/keybindings/rstudio_bindings.json