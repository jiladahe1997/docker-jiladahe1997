FROM nginx

WORKDIR /usr/src/app
COPY ./nginx2.conf ./nginx.conf
CMD ["sh", "-c","nginx -c /usr/src/app/nginx.conf -g \"daemon off;\""]
