# The most lightweight image!
FROM nginx:stable-alpine

# Declare legend... (look below :whale:)
MAINTAINER kadenlnelson@gmail.com

# Copy our configurations and certicates over
RUN mkdir -p /opt/nginx/
COPY . /opt/nginx/
RUN rm /opt/nginx/Dockerfile

# Configure our nginx server
RUN cp /opt/nginx/configurations/nginx.conf /etc/nginx/nginx.conf \
    && cp /opt/nginx/configurations/default.conf /etc/nginx/conf.d/default.conf

# Copy our certficates over
COPY certificates /opt/nginx/
