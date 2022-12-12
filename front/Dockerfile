### BUILD
FROM node:14.21.1-alpine AS build
WORKDIR /usr/src/app
COPY package.json package-lock.json ./
RUN npm install
COPY . .
RUN npm run build --prod

### RUN
FROM nginx:1.22.1-alpine
COPY nginx.conf /etc/nginx/nginx.conf
COPY --from=build /usr/src/app/dist/tlcfront /usr/share/nginx/html
EXPOSE 80
