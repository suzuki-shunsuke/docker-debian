# 日本語対応
# supervisorのインストール
FROM debian:8.2
COPY locale.gen /etc/locale.gen
RUN apt-get update && \
  apt-get install -y locales supervisor && \
  locale-gen && \
  update-locale LANG=ja_JP.UTF-8 && \
  rm -rf /var/lib/apt/lists/*
ENV LANG=ja_JP.UTF-8 TERM=xterm
