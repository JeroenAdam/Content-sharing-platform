# Dev:
 * compte Github Free (répo privé, max. 3 comptes)
 * installation en local (Git, OpenJDK 11, Node.js, Eclipse) https://www.jhipster.tech/installation/
 * communication interne avec RocketChat (hébergé nous-mêmes sur VPS 2GB ram) et sur Github (issues)

# Flow:
 * (laptop dev) commit
 * (VPS 2 GB ram) Jenkins build déclenche dans une VM sur laptop testeur (avec SSH tunnel ouvert), à cause de la compilation Angular besoin >4GB ram, c'est lourd
 * envoi statut build vers Github + Dockerhub push (gratuit)
 * (VM sur laptop testeur) Watchtower > update container en cours
 * (optionnel, VM sur laptop testeur) app temporairement public via le VPS (avec SSH tunnel ouvert)
