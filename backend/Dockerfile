#--------------AFTER DOCKER BEST PRACTICES----------
# code related to build 
FROM node:20 AS builder
WORKDIR /opt/server
COPY code . 
RUN npm install


FROM node:20.18.0-alpine3.20
EXPOSE 8080
RUN addgroup -S expense && adduser -S expense -G expense && \
    mkdir /opt/server && \
    chown -R expense:expense /opt/server
WORKDIR /opt/server
ENV DB_HOST="mysql"
USER expense
CMD ["node","index.js"]
COPY --from=builder /opt/server /opt/server


# -------------------BEFORE BEST PRACTICES------------------
# FROM node:20
# EXPOSE 8080
# ENV DB_HOST="mysql"
# RUN mkdir /opt/server
# WORKDIR /opt/server
# COPY package.json .
# COPY *.js .
# RUN npm install
# CMD ["node", "index.js"]