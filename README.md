# D-ploiement-de-WordPress-avec-Docker-Compose
markdown
 Projet WordPress avec Docker

Bienvenue dans mon petit projet Docker ! Ici, j’ai mis en place un environnement complet pour faire tourner un site WordPress, le tout avec Docker et Docker Compose. C’est simple, propre, et prêt à être lancé en quelques minutes 

---

 Technologies utilisées

-  Docker & Docker Compose
- 🌐 Nginx (serveur web)
- 🐘 MariaDB (base de données)
- 📝 PHP-FPM (WordPress)
- 📦 Volumes pour la persistance

---

 Structure du projet

wordpress-docker/
├── docker-compose.yml
├── nginx-conf/
│   └── default.conf
└── README.md
---
 Déploiement étape par étape (sous Kali Linux)

1 Installer Docker & Docker Compose

bash
sudo apt update
sudo apt install docker.io docker-compose -y
sudo systemctl start docker
sudo systemctl enable docker


2️⃣ Créer le dossier du projet

bash
mkdir wordpress-docker
cd wordpress-docker


3️⃣ Ajouter les fichiers suivants :

- `docker-compose.yml` (configuration des services)
- `nginx-conf/default.conf` (configuration Nginx)
- `README.md` (ce fichier)

4️⃣ Lancer l’environnement

bash
docker-compose up -d
📍 Tu pourras ensuite accéder à WordPress en ouvrant ton navigateur à l’adresse :

👉 http://localhost

---

💾 Volumes utilisés

- wordpress_data : pour garder les fichiers WordPress même après redémarrage
- db_data : pour les données de la base MariaDB

---

🧹 Nettoyage si besoin

- Pour arrêter les conteneurs :

bash
docker-compose down


- Pour tout supprimer (conteneurs + volumes) :

bash
docker-compose down -v


---

👤 Auteur

🧑‍💻 Ramsses Tining  
🎯 Projet réalisé dans le cadre d’un mini-lab DevOps pour apprendre à gérer un site WordPress en conteneur Docker.

