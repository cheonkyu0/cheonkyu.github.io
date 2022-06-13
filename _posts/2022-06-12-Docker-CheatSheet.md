---
title: M1 맥에서 x8664 도커 이미지 빌드 설정하기
author: cheonkyu
date: 2022-06-11 22:10:00 -0500
categories: [Docker]
tags: [M1, Dockerfile]
---


```
# docker-compose.yml
version: '2'

services:
  web:
    build:
    # build from Dockerfile
      context: ./Path
      dockerfile: Dockerfile
    ports:
     - "5000:5000"
    volumes:
     - .:/code
  redis:
    image: redis
```
