FROM python:3.7

COPY . /var/app/etl/
#VOLUME ../messages /var/app/etl/messages/

WORKDIR /var/app/etl/

RUN pip3.7 install -q -r requirements.txt
RUN mkdir /var/log/facebook_messenger/

ENV MYSQL_DATABASE=facebook_messenger \
    MYSQL_USER=jeremy \
    MYSQL_PASSWORD=password \
    MYSQL_PORT=3306 \
    MYSQL_HOST=fbm_db

ENTRYPOINT ["bash", "-c"]
CMD ["/var/app/etl/entrypoint.sh"]
