FROM node:20.18.0-alpine3.20
EXPOSE 8080
RUN mkdir /opt/server
RUN addgroup -S expense && adduser -S expense -G expense
RUN chown -R expense:expense /opt/server
WORKDIR /opt/server
COPY code . 
ENV DB_HOST="mysql"
RUN npm install
USER expense
CMD ["node","index.js"]