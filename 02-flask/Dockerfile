FROM python:2.7

RUN pip install flask \
        gunicorn

ADD ./code /code
EXPOSE 5000

ENV VIRTUAL_HOST flask-demo.foobar.com

WORKDIR /code
CMD gunicorn hello:app -b 0.0.0.0:5000

