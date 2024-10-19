FROM node
EXPOSE 8080
RUN mkdir /opt/server
WORKDIR /opt/server
COPY code . 
ENV DB_HOST="mysql"
RUN npm install 
CMD ["node","index.js"]