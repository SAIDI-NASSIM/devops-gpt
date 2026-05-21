# Utiliser une image Node.js
FROM node:22-alpine

# Définir le répertoire de travail
WORKDIR /app

# Copier package.json et installer les dépendances
COPY package.json ./
RUN npm install

# Copier le reste des fichiers
COPY . .

# Exposer le port pour Vite
EXPOSE 5173

# Lancer le serveur de développement
CMD ["npm", "run", "dev"]
