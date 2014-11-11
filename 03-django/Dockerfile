FROM python:2.7

RUN apt-get install -y libmysqlclient-dev
RUN pip install django \
        mysql-python

ADD ./code /code

# ENV DATABASE_NAME docker_demo
# ENV DATABASE_USER docker_demo
# ENV DATABASE_PASS topsecret
# ENV DATABASE_HOST 1.2.3.4

EXPOSE 8000

WORKDIR /code/docker_demo
CMD gunicorn wsgi:application -b 0.0.0.0:8000
