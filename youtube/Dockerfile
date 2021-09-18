FROM arm64v8/python
# if you are using intel pleae use this
# FROM python

LABEL maintainer="Krish"

RUN pip install --upgrade pip
RUN pip install youtube_dl

COPY ./youtube-dl.conf /etc/youtube-dl.conf

WORKDIR /media

ENTRYPOINT ["youtube-dl"]