# Build with:
#     docker build -t numba_gtc2019:latest .
# Run with:
#     nvidia-docker run -p 8888:8888 -it numba_gtc2019:latest
FROM conda_cuda_base_2019:latest

RUN conda install -y scipy matplotlib pandas

RUN git clone https://github.com/ContinuumIO/gtc2019-numba

WORKDIR ./gtc2019-numba

ARG BRANCH="master"
RUN git fetch && git checkout $BRANCH

CMD jupyter notebook --ip=*
