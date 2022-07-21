# our base image
# Imagem base alterada para alpine por faltar o pacote mysql-client
# Base image changed to alpine due to missing mysql-client package
FROM node:14-alpine

# specify the port number the container should expose
EXPOSE 3001

# User user as root
USER root

# Create App
RUN mkdir /app

# Update Linux Packages
# Usando o gerenciador de pacotes do Alpine Linux para instalar o pacote mysql-client
# Using Alpine Linux package manager to install mysql-client package
RUN apk add --no-cache mysql-client

# Run update and Strongloop install
RUN npm install -g npm
RUN npm install -g pm2
RUN pm2 install pm2-logrotate
