FROM python:3.8.8-slim
COPY . /app
WORKDIR /app
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
        ca-certificates \
        cmake \
        build-essential \
        gcc \
        g++ 

RUN pip install -r requirements.txt
RUN python db_starter.py

CMD gunicorn --bind 0.0.0.0:$PORT wsgi 