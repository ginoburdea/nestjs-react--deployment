FROM node:20
WORKDIR /app

RUN apt-get update
RUN apt-get install git

RUN git clone https://github.com/ginoburdea/nestjs-react--server.git .
RUN npm install

CMD bash -c "DATABASE_URL=$ADMIN_DATABASE_URL npx prisma db push && npm start"