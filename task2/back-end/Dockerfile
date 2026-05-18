# Base sur la dernière image Ubuntu
FROM ubuntu:latest

# Mise à jour et mise à niveau d'APT
RUN apt-get update && apt-get upgrade -y

# Installation de python3 et python3-pip
RUN apt-get install -y python3 python3-pip

# Contournement de la sécurité de pip sur Ubuntu récent (requis par le sujet)
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Installation de Flask via pip3
RUN pip3 install flask

# Définition du répertoire de travail à l'intérieur de l'image
WORKDIR /app

# Copie du script api.py local vers le dossier /app de l'image
COPY ./api.py /app/api.py

# Commande pour lancer le serveur Flask au démarrage du conteneur
CMD ["python3", "api.py"]
