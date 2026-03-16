FROM node:20
WORKDIR /opt/app
COPY package.json /opt/app
COPY *.js /opt/app
RUN npm install
ENV REDIS_HOST="redis" \
    CATALOGUE_HOST="catalogue" \
    CATALOGUE_PORT=8080
CMD ["node","server.js"]


# [Unit]
# Description = Cart Service
# [Service]
# User=roboshop
# // highlight-start
# Environment=REDIS_HOST=<REDIS-SERVER-IP>
# Environment=CATALOGUE_HOST=<CATALOGUE-SERVER-IP>
# Environment=CATALOGUE_PORT=8080
# // highlight-end
# ExecStart=/bin/node /app/server.js
# SyslogIdentifier=cart

# [Install]
# WantedBy=multi-user.target