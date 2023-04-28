FROM tiangolo/uvicorn-gunicorn-fastapi:python3.7
COPY sources.list /etc/apt
RUN pip install -i https://pypi.tuna.tsinghua.edu.cn/simple -U pip aiofiles python-multipart jinja2
COPY /webapp /app