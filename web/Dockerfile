FROM nginx:alpine

RUN apk add fail2ban
COPY fail2ban/filter.d/nextcloud.conf /etc/fail2ban/filter.d/nextcloud.conf
COPY fail2ban/jail.d/nextcloud.local /etc/fail2ban/jail.d/nextcloud.local
RUN rm /etc/fail2ban/jail.d/alpine-ssh.conf
RUN /usr/bin/fail2ban-server -x

COPY server.crt /etc/nginx/server.crt
COPY server.key /etc/nginx/server.key
COPY nginx.conf /etc/nginx/nginx.conf

