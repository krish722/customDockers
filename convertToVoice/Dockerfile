FROM arm64v8/python
# if you are using intel pleae use this
# FROM python

LABEL maintainer="Krish"
WORKDIR /app
COPY convert.py /app/.
RUN pip install --upgrade pip
RUN pip install tqdm google-cloud-texttospeech pypandoc

#RUN apt-get update && apt-get install -y software-properties-common

# Install "ffmpeg"
#RUN add-apt-repository ppa:mc3man/trusty-media
 #RUN add-apt-repository -r ppa:gnome-shell-extensions/ppa
#RUN apt-get update && apt-get install -y ffmpeg
#RUN ln -s /usr/bin/ffmpeg ffmpeg

#COPY ./youtube-dl.conf /etc/youtube-dl.conf
WORKDIR /media


ENTRYPOINT ["python", "/app/convert.py"]