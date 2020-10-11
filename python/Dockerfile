FROM python:3.6

RUN mkdir /code
WORKDIR /code

ADD requirements.txt /code/
RUN pip install --upgrade pip \
    && pip install -r requirements.txt \
    && pip list \
    && wget https://johnvansickle.com/ffmpeg/releases/ffmpeg-release-arm64-static.tar.xz \
    && tar xvf ffmpeg-release-arm64-static.tar.xz \
    && cp ./ffmpeg-4.3.1-arm64-static/ffmpeg /usr/local/bin \
    && cp ./ffmpeg-4.3.1-arm64-static/ffprobe /usr/local/bin \
    && pip install ffmpeg-python

ADD . /code/

