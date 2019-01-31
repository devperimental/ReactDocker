# stage: 1
FROM node:8 as react-build
WORKDIR /react-app
COPY . ./
RUN yarn
RUN yarn build

# stage: 2 — the production environment
FROM nginx:alpine
COPY nginx.conf /etc/nginx/conf.d/default.conf
COPY — from=react-build /react-app/build /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]