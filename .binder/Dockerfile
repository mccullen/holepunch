FROM rocker/binder:4.4.1
LABEL maintainer='your_name'
COPY --chown=${NB_USER} . ${HOME}
USER ${NB_USER}



RUN wget https://github.com/mccullen/holepunch/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2024-07-08/')); devtools::install_deps()"

RUN rm DESCRIPTION.1; exit 0
