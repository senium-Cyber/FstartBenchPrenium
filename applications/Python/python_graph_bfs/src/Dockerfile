FROM python:3.9.0-slim
WORKDIR /usr/src/app
COPY requirements.txt ./
RUN pip3 config set global.index-url http://mirrors.aliyun.com/pypi/simple
RUN pip3 config set install.trusted-host mirrors.aliyun.com
RUN pip3 install --upgrade pip
RUN pip3 install --no-cache-dir -r requirements.txt
RUN pip3 install igraph
COPY . .
# 指定容器启动时运行的命令
CMD ["python", "-u","app.py"]
