FROM node:20
WORKDIR /opt/app
COPY package.json /opt/app
COPY *.js /opt/app
RUN npm install
ENV MONGO="true" \
    MONGO_URL="mongodb://mongodb:27017/catalogue"
CMD ["node","server.js"]


# [Service]
# User=roboshop
# Environment=MONGO=true
# // highlight-start
# Environment=MONGO_URL="mongodb://<MONGODB-SERVER-IPADDRESS>:27017/catalogue"
# // highlight-end
# ExecStart=/bin/node /app/server.js
# SyslogIdentifier=catalogue
