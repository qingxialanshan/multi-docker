FROM node:8.17
WORKDIR "/app"

COPY ./package.json ./
RUN npm install
COPY . .
CMD ["npm","run","start"]