# Utiliser une image Node.js légère
FROM node:22-alpine

# Définir le répertoire de travail dans le conteneur
WORKDIR /app

# Copier les fichiers package.json et package-lock.json
COPY package.json ./

# Installer les dépendances du projet
RUN npm install

# Copier le reste des fichiers de l'application
COPY . .

# Exposer le port sur lequel l'application va tourner
EXPOSE 3000

# La commande pour démarrer l'application
CMD ["node", "index.js"]
