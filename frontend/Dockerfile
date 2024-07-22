# Basis-Image
FROM node:18-alpine

# Arbeitsverzeichnis im Container
WORKDIR /app

# package.json und package-lock.json Dateien kopieren
COPY package*.json ./

# Abhängigkeiten installieren
RUN npm install

# Den Rest der Anwendungscode in das Arbeitsverzeichnis kopieren
COPY . .

# Next.js-Anwendung erstellen
RUN npm run build

# Den Port exponieren, auf dem die App läuft
EXPOSE 3000

# Den Startbefehl definieren 
CMD ["npm", "run", "dev"]
