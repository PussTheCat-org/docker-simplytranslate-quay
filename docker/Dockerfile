FROM alpine:latest

WORKDIR /simplytranslate	
RUN apk upgrade --no-cache && \ 
    apk add --no-cache -t build-dependencies \
      build-base \
      git \
      python3-dev \
      py3-setuptools \
      libffi-dev \
      libxml2-dev && \
    apk add --no-cache \
      python3 \
      py3-pip \
      libxslt-dev && \
    git clone --depth=1 https://codeberg.org/SimpleWeb/SimplyTranslate-Web.git web && \
    cd /simplytranslate/web && \
    pip3 install --no-cache -r requirements.txt && \
    rm -rf /root/.cache && \
    apk del --no-cache build-dependencies

EXPOSE 5000
WORKDIR /simplytranslate/web
CMD ["python3", "main.py"]
