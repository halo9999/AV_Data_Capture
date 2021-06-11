FROM python:slim

RUN apt-get update \
    && apt-get install -y wget ca-certificates \
    && wget -O - 'https://github.com/yoshiko2/AV_Data_Capture/archive/master.tar.gz' | tar xz \
    && mv AV_Data_Capture-master /jav \
    && cd /jav \
    && ( pip install --no-cache-dir -r requirements.txt || true ) \
    && pip install --no-cache-dir requests pyquery lxml Beautifulsoup4 pillow \
    && apt-get purge -y wget

WORKDIR /jav
