FROM python:2-alpine
ENV PYTHONUNBUFFERED 1
RUN mkdir /code
WORKDIR /code

RUN apk --no-cache add --update \
       git \
       libxml2 \
       g++ \
       gcc \
       libxslt-dev \
       libjpeg \
       zlib \
       py-pillow \
       jpeg-dev \
       zlib-dev \
       tzdata \
   && rm -rf /var/cache/apk/*

ENV TZ=Europe/Moscow                                            
RUN addgroup -S web -g 1000 && adduser -u 1000 -G web -D web
USER web
