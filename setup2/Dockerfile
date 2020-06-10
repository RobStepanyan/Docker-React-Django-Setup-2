# React and Node
FROM node:12
RUN mkdir code/
WORKDIR /code
RUN mkdir /frontend
WORKDIR /code/frontend
COPY frontend/package*.json /code/frontend/
RUN npm install
RUN npm run dev
COPY . /code/

# Python
FROM python:3
ENV PYTHONUNBUFFERED 1
WORKDIR /code
COPY requirements.txt /code/
RUN pip install -r requirements.txt