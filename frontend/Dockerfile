FROM node:14.17.0-alpine as node

WORKDIR /app

COPY . .

RUN npm install
RUN npm run build


FROM nginx:alpine
COPY --from=node /app/dist/shop/ /usr/share/nginx/html