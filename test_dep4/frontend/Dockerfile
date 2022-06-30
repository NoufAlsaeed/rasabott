# FROM ubuntu:20.04
# FROM node:17-slim

# RUN apt-get update 
# WORKDIR /app/frontend

# COPY . /app/frontend/

# RUN npm install 

# VOLUME /app/frontend

# CMD npm start


# FROM node
# WORKDIR /app/frontend/
# COPY . /app/frontend/
# RUN npm install
# CMD npm start
# EXPOSE 3000


FROM ubuntu:18.04

RUN apt-get update && apt-get -y install curl gnupg && curl -sL https://deb.nodesource.com/setup_13.x  | bash - && apt-get -y install nodejs


WORKDIR /app/frontend
COPY . /app/frontend

RUN npm install 

VOLUME /app/frontend

CMD npm start