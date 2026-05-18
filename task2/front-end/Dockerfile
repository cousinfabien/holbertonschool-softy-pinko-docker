# Utilise la dernière image officielle de Nginx
FROM nginx:latest

# Copie les fichiers du site web vers le dossier spécifié de l'image
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Écrase la configuration par défaut de Nginx avec notre fichier personnalisé
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf