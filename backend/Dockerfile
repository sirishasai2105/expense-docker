FROM node:20.18.0-alpine3.20
EXPOSE 8080
RUN mkdir /opt/server
WORKDIR /opt/server
COPY code . 
ENV DB_HOST="mysql"
RUN npm install 
CMD ["node","index.js"]