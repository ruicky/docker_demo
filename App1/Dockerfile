FROM registry.cn-hangzhou.aliyuncs.com/zuowenbo/nodejs


# 安装pm2守护进程
RUN npm install pm2 -g -verbose --registry=https://registry.npm.taobao.org

# Create app directory
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app



# Install app dependencies
COPY package.json /usr/src/app/
RUN npm install -verbose --registry=https://registry.npm.taobao.org


# Bundle app source
COPY . /usr/src/app


# 端口
EXPOSE 3100


# 默认执行(可被运行时重写)
CMD ["pm2","start", "ecosystem.config.js","--no-daemon"]

# 构建命令
# docker build -t nodejs_app_1 .

# 运行命令
# docker run -p 3100:3100  -d --name nodejs_app_1 nodejs_app_1
