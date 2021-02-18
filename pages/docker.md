---
title: docker
---

## A nice docker container to create your own python development environment, assuming you have a repredefined requirements file.
###
```Docker
FROM python:3.8.0
RUN apt-get update -y
RUN apt-get install -y python-pip python-dev build-essential
RUN pip install --upgrade pip
RUN apt-get install -y ghostscript libgs-dev
RUN apt-get install -y libmagickwand-dev imagemagick --fix-missing
RUN apt-get install -y libpng-dev zlib1g-dev libjpeg-dev
RUN apt-get install -y nano
WORKDIR /usr/src/app
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt
```
###
## How to build smaller stage dockers with staged multi-build : https://pythonspeed.com/articles/smaller-python-docker-images/
### Write summary here:
##
## [[docker-compose]] is a framework for managing entire project [[docker]] builds and is very useful for [[Devops]] [[Development]]
##
##
