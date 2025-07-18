FROM ubuntu:24.04

ENV DEBIAN_FRONTEND=noninteractive

# install texlive
RUN apt-get update && apt-get install -y \
    latexmk \
    language-pack-ja \
    texlive-latex-base \
    texlive-lang-japanese \
    texlive-latex-recommended \
    texlive-latex-extra \
    texlive-fonts-recommended \
    texlive-extra-utils \
    xzdec

RUN apt-get install -y \
    cpanminus \
    make \
    perl \
    git \
    wget 

# clean up
RUN rm -rf /var/lib/apt/lists/* \
    && apt-get clean

RUN tlmgr init-usertree
RUN kanji-config-updmap-sys ipaex
RUN cpanm Log::Log4perl Log::Dispatch::File YAML::Tiny File::HomeDir Unicode::GCString

CMD ["bash"]
