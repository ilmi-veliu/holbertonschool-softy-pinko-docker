# Utiliser Ubuntu comme base
FROM ubuntu:latest

# Mettre à jour APT
RUN apt-get update
RUN apt-get upgrade -y

# Installer Python3 et pip3
RUN apt-get install -y python3 python3-pip

# Corriger le problème EXTERNALLY-MANAGED si besoin
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED || true

# Installer Flask via pip3
RUN pip3 install flask

# Définir /app comme dossier de travail
WORKDIR /app

# Copier ton fichier api.py dans l’image
COPY ./api.py /app/api.py

# Lancer Flask
CMD ["python3", "api.py"]
