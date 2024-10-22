#FROM nginx:mainline-alpine3.20-slim
FROM nginx:1.27.2 mainline-alpine-slim
COPY code /usr/share/nginx/html
RUN rm -rf /etc/nginx/nginx.conf
RUN rm -rf /etc/nginx/conf.d/default.conf
COPY expense.conf /etc/nginx/nginx.conf

