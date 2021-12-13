FROM node:16.13.1-alpine AS builder

WORKDIR /opt/web
#COPY package.json package-lock.json ./
#RUN npm install

# add .bin to $PATH
#ENV PATH="./node_modules/.bin:$PATH"

COPY . ./
RUN npm install
RUN npm run build

FROM nginx:1.17-alpine
COPY nginx.conf /etc/nginx/nginx.conf
COPY --from=builder /opt/web/dist/frontend /usr/share/nginx/html
