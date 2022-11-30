# Web-App mit Content und mit Rueckmeldung welcher Container (ID) die Anfrage bearbeitet hat
# Linux x64
FROM node:current-alpine

# LABEL org.opencontainers.image.title="Hallo in der Containerwelt!" \
#      org.opencontainers.image.description="Webserver-Content inkl. Container-ID" \
#      org.opencontainers.image.authors="@calisto"

# Erstelle das Directory im Container-Image fuer den App-Code
RUN mkdir -p /usr/src/app

# Copy App-Code (.) ins /usr/src/app im Container-Image
COPY . /usr/src/app

# Setze das Working-Directory in den Context
WORKDIR /usr/src/app

# Installiere dependencies von packages.json
RUN npm install

# Kommando um den Container auszufuehren
ENTRYPOINT [ "node", "app.js" ]