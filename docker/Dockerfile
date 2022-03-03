FROM alpine:latest

WORKDIR /simplytranslate	
RUN apk upgrade --no-cache && \ 
    apk add --no-cache -t build-dependencies \
      build-base \
      git \
      py3-setuptools \
      libffi-dev \
      libxml2-dev && \
    apk add --no-cache \
      python3 \
      py3-pip \
      libxslt-dev && \
    git clone --depth=1 https://git.sr.ht/~metalune/simplytranslate_engines engines && \
    git clone --depth=1 https://git.sr.ht/~metalune/simplytranslate_web web && \
    cd  /simplytranslate/engines && \
    python3 setup.py install && \
    pip3 install --upgrade pip wheel setuptools && \
    pip3 install --no-cache -r requirements.txt && \
    cd /simplytranslate/web && \
    pip3 install --no-cache -r requirements.txt && \
    rm -rf /root/.cache && \
    apk del --no-cache build-dependencies

EXPOSE 5000
WORKDIR /simplytranslate/web
CMD ["python3", "main.py"]
