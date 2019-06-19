FROM python:3.6.8-slim-stretch

COPY . /var/www/src/

RUN mkdir -p /var/www/src \
    && chown -R nobody:nogroup /var/www/
VOLUME /var/www/data

RUN pip install -r /var/www/src/requirements.txt

USER nobody
WORKDIR /var/www/src/

EXPOSE 5000
CMD ["python", "__main__.py"]