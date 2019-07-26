# Docker Instructions

To build the images:

```bash
docker build -t conda_cuda_base_2019:latest ./base
docker build -t numba_gtc2019:latest ./notebooks
```

The notebook image takes an optional build argument `BRANCH` to
select the branch or commit to checkout

```
docker build -t numba_gtc2019:latest --build-arg BRANCH=master ./notebooks
```

Run the notebook with:

```bash
nvidia-docker run -p 9999:9999 -it numba_gtc2019:latest
```

It will start the jupyter notebook automatically.
