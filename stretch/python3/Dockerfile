FROM python:3-stretch
ENV PYTHONUNBUFFERED 1
RUN mkdir /code
RUN mkdir /home/web
WORKDIR /code

RUN apt-get update && apt-get install -y \
    git \
    bash \
    libxml2 \
    g++ \
    gcc \
    libxslt-dev \
    libjpeg-dev \
    python-pillow \
    zlib1g \
    tzdata \
    && rm -rf /var/lib/apt/lists/*

ENV TZ=Europe/Moscow                                            
RUN groupadd  -g 1000 web && useradd --no-log-init -d /home/web -r -u 1000 -g web web
RUN chown web:web /home/web
USER web
