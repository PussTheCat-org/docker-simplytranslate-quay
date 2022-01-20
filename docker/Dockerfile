FROM alpine:3.15

WORKDIR /usr/local/simplytranslate	
RUN apk upgrade --no-cache \
    && apk add --no-cache -t build-dependencies \
       build-base \
       py3-setuptools \
       python3-dev \
       libffi-dev \
       libxml2-dev \
       git \
    && apk add --no-cache python3 py3-pip libxslt-dev && \
    git clone --depth=1 https://git.sr.ht/~metalune/simplytranslate_engines engines && \
    git clone --depth=1 https://git.sr.ht/~metalune/simplytranslate_web web && \
    cd  /usr/local/simplytranslate/engines && \
    python3 setup.py install && \
    pip3 install --upgrade pip wheel setuptools && \
    pip3 install --no-cache -r requirements.txt && \
    cd /usr/local/simplytranslate/web && \
     pip3 install --no-cache -r requirements.txt && \
    rm -rf /root/.cache && \
    apk del --no-cache build-dependencies

EXPOSE 5000
WORKDIR /usr/local/simplytranslate/web
CMD ["python3", "main.py"]
