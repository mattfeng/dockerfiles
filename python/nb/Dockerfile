FROM nvidia/cuda:10.2-cudnn8-devel-ubuntu18.04

RUN apt-get update && apt-get install -y  \
    build-essential libssl-dev libffi-dev \
    python3-dev python3-pip               \
    python3-virtualenv

RUN ln -s $(which python3) /usr/bin/python
RUN ln -s $(which pip3) /usr/bin/pip

RUN pip install                           \
    jupyter numpy scipy matplotlib        \
    scikit-learn sympy

RUN mkdir /nb
WORKDIR /nb

ENTRYPOINT ["jupyter", "notebook", "/nb", "--ip", "0.0.0.0", "--port", "8080", "--no-browser", "--allow-root"]
