#  Docker环境执行chat_gradio.py

系统需要准备的环境

+ docker： 24.0.2
+ docker-compose

## 1. 准备Docker镜像

通过docker容器可以更方便的管理需要安装的环境依赖。所以这里可以直接通过docker容器启动[chat_gradio](../examples/chat_gradio.py)

```bash
git clone https://github.com/FlagAlpha/Llama2-Chinese.git

cd Llama2-Chinese

sudo docker build -f docker/Dockerfile  -t FlagAlpha/llama2-chinese-7b:gradio .
```

## 2. 通过docker-compose启动chat_gradio


```bash
cd Llama2-Chinese/docker
doker-compose up -d --build
```