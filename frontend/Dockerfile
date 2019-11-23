FROM ubuntu:16.04
LABEL author="Truong Bui Van"


WORKDIR /root
COPY . .

RUN apt update -y
RUN apt install curl -y
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs

RUN npm install
EXPOSE 5000

#CMD [ "npm", "run", "start:${FRONT_URL}" ]
CMD API_URL=${API_URL} npm start
