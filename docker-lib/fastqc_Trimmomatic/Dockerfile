FROM registry.cn-beijing.aliyuncs.com/90wukai/bioinfo:base

RUN mkdir -p /bioapp/fastqc_Trimmomatic
WORKDIR /bioapp/fastqc_Trimmomatic

RUN wget "https://www.bioinformatics.babraham.ac.uk/projects/fastqc/fastqc_v0.11.7.zip"
RUN unzip fastqc_v0.11.7.zip && \
        rm  fastqc_v0.11.7.zip && cd FastQC/ && chmod 755 fastqc
ENV PATH=$PATH:/bioapp/fastqc_Trimmomatic/FastQC/

RUN wget "http://www.usadellab.org/cms/uploads/supplementary/Trimmomatic/Trimmomatic-0.36.zip"
RUN unzip Trimmomatic-0.36.zip && \
    rm Trimmomatic-0.36.zip
