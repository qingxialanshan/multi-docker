FROM node:8.17 as builder
WORKDIR '/app'
COPY ./package.json ./
RUN npm install
COPY . .
RUN npm run build

FROM nginx
EXPOSE 3000
COPY ./nginx/default.conf /etc/nginx/config/default.conf
COPY --from=builder /app/build /usr/share/nginx/html
