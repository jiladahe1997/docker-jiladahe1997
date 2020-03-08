FROM tiangolo/nginx-rtmp

WORKDIR /usr/src/app
COPY ./nginx.conf ./nginx.conf

RUN mkdir /tmp/api/music/stream -p
CMD ["sh", "-c","nginx -c /usr/src/app/nginx.conf -g \"daemon off;\""]
