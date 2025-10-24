# Étape 1 : Utiliser une image de base nginx
FROM nginx:alpine

# Étape 2 : Copier ton fichier index.html dans le dossier par défaut de nginx
COPY index.html /usr/share/nginx/html/index.html

# Étape 3 : Exposer le port 80 (port HTTP)
EXPOSE 80

# Étape 4 : Lancer nginx
CMD ["nginx", "-g", "daemon off;"]

