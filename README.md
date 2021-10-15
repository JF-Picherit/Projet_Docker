# TP Projet Docker

### Description du projet :  

Le projet consiste à faire comuniquer 4 container dans un environement Docker.
Pour fair cela j'ai choisit un projet de test en début de développement.
Il s'agit d'une application type le bon coin mais pour les camions.

Pour lancer le projet : ``docker-compose up --build``


Puis diriger vous vers : ``http://localhost:3053/``

![alt Exemple application](./images/Exemple1.PNG) 

Cette aplication à besoin :

- d'un front ***React*** 
- d'un back api ***NodeJs*** 
- et une base ***postgres*** avec qui comuniquer.

![alt Exemple application](./images/Shema1.png) 

Pour réaliser à bien cela, pour gérer plusieurs connection en même temps je me suis aidé de ***NGINX***. J'ai ainsi pu gérer les différents paramètres de proxy, port et path pour mon api.

![alt Exemple shema ilustration](./images/solution.png)  

J'ai ainsi deux volumes.

- Un volume server pour mon Api.
- Un volume client pour mon front.

Dans ces deux volumes on peux y retrouver un dockerfile permettant l'installation du node-module et le lancement du projet.

J'utilise l'image postgres sur laquel dépend mon api pour fonctionner.
Ainsi c'est mon api qui vas fournirtoutes les variable d'environement nécessaire à la cnnexion à ma base de donnée postgre.



