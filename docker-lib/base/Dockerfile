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
    #apt-get install -y openjdk-8-jdk && \
    #update-alternatives --config java && \
    #update-alternatives --config javac && \
RUN apt-get clean
RUN apt-get purge

# pip
RUN pip install -U pip
RUN pip install biopython
