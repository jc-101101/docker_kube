FROM node:16-alpine as stage1
WORKDIR '/var/johnsonchan/frontend'
COPY package.json .
RUN npm install
COPY . .

FROM nginx 
COPY --from=stage1 /var/johnsonchan/frontend/build /usr/share/nginx/html
