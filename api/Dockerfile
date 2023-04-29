FROM pytorch/pytorch:latest
COPY sources.list /etc/apt

WORKDIR /app
RUN apt-get update
RUN apt-get install ffmpeg libsm6 libxext6 -y
COPY requirements.txt requirements.txt
RUN pip install -i https://pypi.tuna.tsinghua.edu.cn/simple -U pip
RUN pip install -i https://pypi.tuna.tsinghua.edu.cn/simple -r requirements.txt
COPY . .
RUN rm -r /app/api/uploads/*; exit 0
RUN rm -r /app/api/static/*; exit 0