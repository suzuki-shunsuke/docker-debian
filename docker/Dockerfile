# nginxのインストール
FROM quay.io/suzuki_shunsuke0/debian:base
RUN apt-get update && \
  apt-get install -y wget && \
  wget http://nginx.org/keys/nginx_signing.key && \
  apt-key add nginx_signing.key && \
  echo "deb http://nginx.org/packages/debian/ jessie nginx" >> /etc/apt/sources.list && \
  echo "deb-src http://nginx.org/packages/debian/ jessie nginx" >> /etc/apt/sources.list && \
  apt-get update && \
  apt-get install -y nginx && \
  rm nginx_signing.key && \
  rm -rf /var/lib/apt/lists/*
# RUN mkdir -p /var/log/supervisor/nginx
# COPY supervisor/conf.d/ /etc/supervisor/conf.d/
# COPY supervisor/supervisord.conf /etc/supervisor/
# COPY nginx.conf .htpasswd /etc/nginx/
# RUN chmod 644 /etc/nginx/.htpasswd
# WORKDIR /home/debian
# RUN chown -R debian:debian /home/debian
# EXPOSE 80 443
# CMD /usr/bin/supervisord -c /etc/supervisor/supervisord.conf
