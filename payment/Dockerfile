FROM python:3.9
EXPOSE 8080
WORKDIR /opt/app
COPY payment.ini .
COPY *.py .
COPY requirements.txt .
RUN pip3 install -r requirements.txt
ENV CART_HOST="cart" \
    CART_PORT="8080" \
    USER_HOST="user" \
    USER_PORT="8080" \
    AMQP_USER="roboshop" \
    AMQP_PASS="roboshop123"
CMD ["uwsgi","--ini","payment.ini"]


# [Unit]
# Description=Payment Service

# [Service]
# User=root
# WorkingDirectory=/app
# // highlight-start
# Environment=CART_HOST=<CART-SERVER-IPADDRESS>
# Environment=CART_PORT=8080
# Environment=USER_HOST=<USER-SERVER-IPADDRESS>
# Environment=USER_PORT=8080
# Environment=AMQP_HOST=<RABBITMQ-SERVER-IPADDRESS>
# // highlight-end
# Environment=AMQP_USER=roboshop
# Environment=AMQP_PASS=roboshop123

# ExecStart=/usr/local/bin/uwsgi --ini payment.ini
# ExecStop=/bin/kill -9 $MAINPID
# SyslogIdentifier=payment

# [Install]
# WantedBy=multi-user.target