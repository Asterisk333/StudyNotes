# Basic Setup

> [⬅️**back**](./README.md)

### Dockerfile

FROM    -> Defines the Basic Image  
RUN     -> Executes a command like: 'mkdir' or 'npm install'  
COPY    -> Copies, usually . to the work dir  
WORKDIR -> Sets the Working directory  
ENCRYPT -> Runs the container  

```
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
```
https://web.microsoftstream.com/video/b4143f73-2f96-446d-ba66-c44e8ddcb270?referrer=https:%2F%2Fteams.microsoft.com%2F


---

