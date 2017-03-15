FROM index.tenxcloud.com/docker_library/nginx

ADD app1.conf /etc/nginx/conf.d/app1.conf
ADD app2.conf /etc/nginx/conf.d/app2.conf

EXPOSE 80 443

CMD ["nginx", "-g", "daemon off;"]


# 构建命令
# docker build -t test_nginx .

# 运行命令
# docker run -p 80:80  -d --name test_nginx test_nginx





