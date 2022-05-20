# `cellxgene-gateway`

## Build Docker image

```sh
docker build -t cellxgene-gateway .
```

## Run

```sh
docker run -it --rm \
-v <dir_with_h5ad_files>:/cellxgene-data \
-p 5005:5005 \
cellxgene-gateway
```

Open <http://0.0.0.0:5005> in browser.

## Notes

- `.h5ad` files in data directory can be organized in sub-directories
- The app provides an overview of all datasets at: <http://0.0.0.0:5005/filecrawl.html>
- The app provides an overview of currently running instances at: <http://0.0.0.0:5005/cache_status>
- Navigating to the URL of a specific dataset, e.g. `http://0.0.0.0:5005/view/test/pbmc3k.h5ad/`, will trigger the launch of a cellxgene instance, which will be shown once it is ready.
