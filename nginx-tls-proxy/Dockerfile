FROM nginx
COPY ssl-proxy.conf /etc/nginx/conf.d/
#COPY ssl-proxy.conf /etc/nginx/conf.d/default.conf
RUN openssl req -x509 -batch -nodes -days 365 -newkey rsa:2048 -keyout /etc/nginx/rocketchat-certificate.key -out /etc/nginx/rocketchat-certificate.crt
RUN chmod 400 /etc/nginx/rocketchat-certificate.key
RUN openssl dhparam -out /etc/nginx/dhparams.pem 2048
