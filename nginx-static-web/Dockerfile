FROM nginx:stable-alpine
MAINTAINER Shogo Iwano <shiwano@gmail.com>

COPY ./nginx.conf /etc/nginx/nginx.conf

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
