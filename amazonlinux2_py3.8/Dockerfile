FROM amazonlinux:2.0.20200207.1

RUN cd /opt && \
    yum install -y gcc openssl-devel bzip2-devel libffi-devel wget tar gzip make && \
    wget https://www.python.org/ftp/python/3.8.2/Python-3.8.2.tgz && \
    tar xzf Python-3.8.2.tgz && \
    cd Python-3.8.2 && \
    ./configure --enable-optimizations && \
    make altinstall && \
    rm -f /opt/Python-3.8.2.tgz && \
    echo "alias python3=python3.8" > ~/.bashrc