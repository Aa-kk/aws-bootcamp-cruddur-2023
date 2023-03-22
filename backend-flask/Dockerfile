# Build stage
FROM python:3.10-slim-buster AS build

WORKDIR /backend-flask

COPY requirements.txt requirements.txt
RUN pip3 install --no-cache-dir --prefix=/install -r requirements.txt

COPY . .

# Runtime stage
FROM python:3.10-slim-buster

ENV FLASK_APP=app.py
ENV FLASK_ENV=production 
RUN apt-get -y update 
RUN apt-get -y install curl
COPY --from=build /install /usr/local

COPY . .

EXPOSE ${PORT}

CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]
