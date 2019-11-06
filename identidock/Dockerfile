FROM python:3.6

RUN groupadd -r uwsgi && useradd -r -g uwsgi uwsgi
RUN pip install Flask uWSGI requests redis
WORKDIR /app
COPY cmd.sh /
COPY app /app


EXPOSE 9090 9191
USER uwsgi

CMD ["/cmd.sh"]
