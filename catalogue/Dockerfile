
FROM node:18
EXPOSE 8080
#RUN addgroup -S roboshop && adduser -S roboshop -G roboshop
RUN addgroup -g 1001 roboshop && adduser -D -u 1001 -G roboshop roboshop
WORKDIR /opt/server
ENV MONGO=true
RUN chown roboshop:roboshop /opt/server
USER roboshop
COPY package.json /opt/server/
COPY server.js /opt/server/
RUN npm install
CMD ["node", "server.js"]