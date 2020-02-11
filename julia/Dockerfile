FROM julia

RUN apt-get -y update
RUN apt-get install -y wget

RUN useradd -ms /bin/bash eager
USER eager

RUN wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda.sh
RUN bash ~/miniconda.sh -b -p $HOME/miniconda
RUN echo 'export PATH=~/miniconda/bin:$PATH' >> ~/.bashrc
ENV PATH="/home/eager/miniconda/bin:${PATH}"

RUN pip install jupyter

RUN julia -e "using Pkg; Pkg.add(\"IJulia\")"
RUN julia -e "using Pkg; Pkg.add(\"WebIO\"); using WebIO; WebIO.install_jupyter_nbextension()"
RUN julia -e "using Pkg; Pkg.add(\"Plots\")"
RUN julia -e "using Pkg; Pkg.add(\"Interact\")"
RUN julia -e "using IJulia"

