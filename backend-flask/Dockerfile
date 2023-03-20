FROM python:3.10-slim-buster

WORKDIR /backend-flask

COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

COPY . .

ENV FLASK_ENV=development

EXPOSE ${PORT}

# Make flask_run.py script executable 
RUN chmod +x /backend-flask/flask_run.py
ENTRYPOINT ["/backend-flask/flask_run.py"]

# CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]
