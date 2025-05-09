# docker/Dockerfile
# FROM nginx:alpine
# COPY ../app/index.html /usr/share/nginx/html/index.html
# docker/Dockerfile
FROM nginx:alpine

# Copy the custom NGINX configuration file
COPY nginx.conf /etc/nginx/conf.d/default.conf

# Copy the index.html file
COPY ../app/index.html /usr/share/nginx/html/index.html

