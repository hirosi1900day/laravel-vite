FROM nginx:1.18.0

# インクルード用のディレクトリ内を削除
RUN rm -f /etc/nginx/conf.d/*

# Nginxの設定ファイルをコンテナにコピー
ADD ./default.conf /etc/nginx/conf.d/default.conf
# for health check
RUN apt-get update && apt-get install -y curl
# ビルド完了後にNginxを起動
CMD /usr/sbin/nginx -g 'daemon off;' -c /etc/nginx/nginx.conf