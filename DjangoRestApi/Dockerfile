FROM python:3.11

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

WORKDIR /app

COPY requirements.txt /app/
RUN pip install --no-cache-dir -r requirements.txt

COPY . /app/

ARG DOMAIN
ENV DJANGO_ALLOWED_HOSTS=$DOMAIN

EXPOSE 8080

CMD ["python", "manage.py", "runserver", "0.0.0.0:8080"]
