FROM ubuntu:14.04
RUN apt-get clean all  && \
    apt-get update     && \
    apt-get install -y software-properties-common && \
    add-apt-repository ppa:openjdk-r/ppa   && \
    apt-get update  && \
    apt-get upgrade -y && \
    apt-get install -y    \
        autotools-dev     \
        automake          \
        cmake             \
        curl              \
        fuse              \
        git               \
        wget              \
        zip               \
        build-essential   \
        gcc               \
        pkg-config        \
        python2.7         \
	python-dev        \
        python-pip        \
        libncurses5-dev   \
        libncursesw5-dev  \
        libboost-all-dev  \
        zlib1g-dev
RUN apt-get install -y openjdk-8-jdk

RUN apt-get clean
RUN apt-get purge

# pip
ENV PIP_INDEX_URL=http://pypi.douban.com/simple/
ENV PIP_TRUSTED_HOST=pypi.douban.com
RUN pip install -U pip
RUN pip install biopython

RUN apt-get install -y vim

