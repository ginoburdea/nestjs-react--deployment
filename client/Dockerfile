FROM node:20
WORKDIR /app

RUN apt-get update
RUN apt-get install git

RUN git clone https://github.com/ginoburdea/nestjs-react--client.git .
RUN npm install

COPY .env .env.local
RUN npm run build
RUN rm .env.local

CMD npm start