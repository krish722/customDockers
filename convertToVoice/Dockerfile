FROM arm64v8/python
# if you are using intel pleae use this
# FROM python

LABEL maintainer="Krish"
WORKDIR /app
COPY convert.py /app/.
RUN pip install --upgrade pip
RUN pip install tqdm google-cloud-texttospeech pypandoc

WORKDIR /media

ENTRYPOINT ["python", "/app/convert.py"]