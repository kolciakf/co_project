FROM node:14-alpine AS builder 
WORKDIR /app
COPY ./ ./
RUN npm install
RUN npm run build

FROM nginx:1.15 AS http
COPY --from=builder /app/build/ /usr/share/nginx/html/




