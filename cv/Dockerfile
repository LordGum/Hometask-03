FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
    texlive-latex-base \
    texlive-latex-extra \
    texlive-fonts-recommended \
    texlive-lang-cyrillic \
    texlive-fonts-extra \
    cm-super \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /resume

COPY CV/ /resume/

CMD pdflatex -interaction=nonstopmode main.tex