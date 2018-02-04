FROM registry.cn-beijing.aliyuncs.com/90wukai/bioinfo:base

RUN mkdir -p /bioapp/ncbi
WORKDIR /bioapp/ncbi

RUN wget ftp://ftp.ncbi.nlm.nih.gov/blast/executables/blast+/2.4.0/ncbi-blast-2.4.0+-x64-linux.tar.gz
RUN tar -zxvf ncbi-blast-2.4.0+-x64-linux.tar.gz && \
        rm  ncbi-blast-2.4.0+-x64-linux.tar.gz
ENV PATH=$PATH:/bioapp/ncbi/ncbi-blast-2.4.0+/bin/

RUN wget https://ftp-trace.ncbi.nlm.nih.gov/sra/sdk/current/sratoolkit.current-ubuntu64.tar.gz
RUN tar -zxvf sratoolkit.current-ubuntu64.tar.gz && \
    rm sratoolkit.current-ubuntu64.tar.gz
ENV PATH=$PATH:/bioapp/ncbi/sratoolkit.2.8.2-1-ubuntu64/bin/

RUN wget http://download.asperasoft.com/download/sw/connect/3.7.4/aspera-connect-3.7.4.147727-linux-64.tar.gz
RUN tar -zxvf aspera-connect-3.7.4.147727-linux-64.tar.gz
RUN bash ./aspera-connect-3.7.4.147727-linux-64.sh && \
    cp ~/.aspera/connect/etc/aspera-license /usr/local/bin/ && cp /root/.aspera/connect/etc/asperaweb_id_dsa.openssh /bioapp/ncbi && \
    rm ./aspera-connect-3.7.4.147727-linux-64.tar.gz ./aspera-connect-3.7.4.147727-linux-64.sh
ENV PATH=$PATH:/root/.aspera/connect/bin/

RUN wget ftp://ftp.ncftp.com/ncftp/binaries/ncftp-3.2.6-linux-x86_64-glibc2.17-export.tar.gz
RUN tar -zxvf ncftp-3.2.6-linux-x86_64-glibc2.17-export.tar.gz && \
    rm ncftp-3.2.6-linux-x86_64-glibc2.17-export.tar.gz
ENV PATH=$PATH:/bioapp/ncbi/ncftp-3.2.6/bin
