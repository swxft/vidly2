FROM node:14.16.0-alpine3.13

RUN addgroup app && adduser -S -G app app
USER app

WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . . 
#RUN chmod +x /app/docker-entrypoint.sh 
EXPOSE 3001 
ENTRYPOINT ["sh", "/app/docker-entrypoint.sh"]
CMD ["npm", "start"]