FROM nathanhillyer/ubuntu-base
ENV LANG C.UTF-8
RUN PIP_INSTALL="python -m pip install --upgrade --no-cache-dir --retries 10 --timeout 60" && \
    $PIP_INSTALL \
        collageradiomics==0.0.1a35 \
        && \
    ldconfig && \
    apt-get clean && \
    apt-get autoremove && \
    rm -rf /var/lib/apt/lists/* /tmp/* ~/*
CMD jupyter notebook --no-browser --ip=0.0.0.0 --allow-root --NotebookApp.token= --notebook-dir='/root'
EXPOSE 8888