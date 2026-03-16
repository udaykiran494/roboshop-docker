FROM node:20
WORKDIR /opt/app
EXPOSE 8080
COPY package.json .
COPY *.js .
RUN npm install
ENV MONGO="true" \
    REDIS_URL='redis://redis:6379' \
    MONGO_URL="mongodb://mongodb:27017/users"
CMD ["node","server.js"]


# [Unit]
# Description = User Service
# [Service]
# User=roboshop
# Environment=MONGO=true
# // highlight-start
# Environment=REDIS_URL='redis://<REDIS-IP-ADDRESS>:6379'
# Environment=MONGO_URL="mongodb://<MONGODB-SERVER-IP-ADDRESS>:27017/users"
# // highlight-end
# ExecStart=/bin/node /app/server.js
# SyslogIdentifier=user