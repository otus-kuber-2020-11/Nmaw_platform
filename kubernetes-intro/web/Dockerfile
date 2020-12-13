FROM nginx:1.18-alpine

WORKDIR /app
COPY . /app

COPY ./nginx.conf /etc/nginx/conf.d/default.conf

EXPOSE 8000

