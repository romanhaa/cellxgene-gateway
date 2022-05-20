FROM python:3.9

RUN pip install git+https://github.com/Novartis/cellxgene-gateway 'MarkupSafe<2.1'
  # mkdir /cellxgene-data \
  # wget https://raw.githubusercontent.com/chanzuckerberg/cellxgene/master/example-dataset/pbmc3k.h5ad -O /cellxgene-data/pbmc3k.h5ad

ENV CELLXGENE_DATA=/cellxgene-data
ENV CELLXGENE_LOCATION=/usr/local/bin/cellxgene

CMD ["cellxgene-gateway"]
