FROM python:slim-bullseye

ENV PYTHONUNBUFFERED=1
ENV PYTHONDONTWRITEBYTECODE=1

RUN pip install --upgrade pip
RUN pip install flask

WORKDIR /app

COPY ./server.py .

CMD [ "flask", "--app", "server", "run", "--host=0.0.0.0" ]

EXPOSE 5000