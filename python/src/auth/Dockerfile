FROM python:3.10.14

RUN apt-get update \
    && apt-get install -y --no-install-recommends --no-install-suggests \
    build-essentails default-libmysqlclient-dev \
    && pip insatll --no-cache-dir --upgrade pip

WORKDIR /app
COPY ./requirements.txt /app
RUN pip install --no-cache-dir --requirements /app/requirements.txt
COPY . /app

EXPOSE 5000

CMD ["python3", "server.py"]