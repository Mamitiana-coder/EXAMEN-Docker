# Fiche de Commandes Docker

## Commandes de Base
```bash
docker --version          # Vérifier la version
docker info               # Informations système
docker stats              # Statistiques en direct
```

## Gestion des Images
```bash
docker images             # Lister les images locales
docker pull <image>       # Télécharger une image (ex: `nginx`)
docker rmi <image>        # Supprimer une image
docker image prune        # Nettoyer les images inutilisées
docker build -t <nom> .   # Construire une image depuis un Dockerfile
```

## Gestion des Conteneurs
```bash
docker run -d -p <host:container> --name <nom> <image>  # Lancer un conteneur
docker ps -a                # Lister tous les conteneurs
docker start <conteneur>    # Démarrer un conteneur
docker stop <conteneur>     # Arrêter un conteneur
docker restart <conteneur>  # Redémarrer un conteneur
docker rm <conteneur>       # Supprimer un conteneur
docker rm -f $(docker ps -aq)  # Tout supprimer (forcer)
```

## Inspection
```bash
docker logs <conteneur>         # Afficher les logs
docker logs -f <conteneur>      # Suivre les logs
docker inspect <conteneur>      # Détails techniques
docker exec -it <conteneur> bash  # Shell interactif
```
