FROM node:14.16.0-alpine3.13
RUN sudo chown -R $USER /usr/local/lib/node_modules
RUN addgroup app && adduser -S -G app app
USER app

WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .

EXPOSE 3000 

CMD ["npm", "start"]