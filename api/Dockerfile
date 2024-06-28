# Utilisez l'image officielle Node.js comme image de base
FROM node:17

# Définir le répertoire de travail dans le conteneur
WORKDIR /usr/src/app

# Copier les fichiers package.json et package-lock.json dans le répertoire de travail
COPY package*.json ./

# Nettoyer le cache npm et installer les dépendances
RUN npm cache clean --force && npm install --force

# Copier le reste de l'application dans le répertoire de travail
COPY . .

# Exposer le port sur lequel l'application écoute
EXPOSE 3000

# Démarrer l'application
CMD ["node", "app.js"]