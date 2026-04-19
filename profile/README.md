# 🎓 CampusHub - Écosystème de Gestion Académique SaaS

<p align="center">
  <img src="https://img.shields.io/badge/CampusHub-Organization-blue?style=for-the-badge&logo=appveyor" alt="CampusHub Banner" />
</p>

> **CampusHub** est une plateforme SaaS (Software as a Service) de nouvelle génération conçue pour révolutionner la gestion académique. En centralisant les ressources, en automatisant la planification et en activant la communication temps réel, CampusHub offre une expérience fluide et professionnelle aux étudiants, enseignants, doyens et administrateurs.

---

## ✨ Vision & Valeurs

Notre mission est de transformer l'administration universitaire complexe en un système agile, transparent et moderne. CampusHub n'est pas seulement une application, c'est une infrastructure complète pensée pour la scalabilité et la performance.

- 🚀 **Performance** : Architecture microservices distribuée.
- 📱 **Accessibilité** : Expérience utilisateur "Mobile-First" et "SaaS Pro".
- 🔔 **Temps Réel** : Notifications instantanées via WebSockets et RabbitMQ.
- 🛡️ **Sécurité** : Authentification centralisée et contrôle d'accès granulaire (RBAC).

---

## 🛠️ Stack Technologique de l'Organisation

L'écosystème CampusHub repose sur les technologies les plus robustes du marché pour garantir une fiabilité de niveau entreprise.

| Secteur | Technologies |
| :--- | :--- |
| **Backend Core** | ![Java](https://img.shields.io/badge/Java-17-ED8B00?style=flat-square&logo=java&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.2.5-6DB33F?style=flat-square&logo=spring-boot&logoColor=white) ![Node.js](https://img.shields.io/badge/Node.js-18-339933?style=flat-square&logo=nodedotjs&logoColor=white) |
| **Frontend** | ![React](https://img.shields.io/badge/React-18-20232A?style=flat-square&logo=react&logoColor=61DAFB) ![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat-square&logo=typescript&logoColor=white) ![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white) |
| **Data & Cache** | ![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?style=flat-square&logo=mysql&logoColor=white) ![Sequelize](https://img.shields.io/badge/Sequelize-6.x-52B0E7?style=flat-square&logo=sequelize&logoColor=white) |
| **Messaging** | ![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=flat-square&logo=rabbitmq&logoColor=white) ![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=flat-square&logo=socketdotio&logoColor=white) |
| **Infrastructure** | ![Docker](https://img.shields.io/badge/Docker-Enabled-2496ED?style=flat-square&logo=docker&logoColor=white) ![Kubernetes](https://img.shields.io/badge/Kubernetes-K8s-326CE5?style=flat-square&logo=kubernetes&logoColor=white) ![Spring Cloud](https://img.shields.io/badge/Spring_Cloud-Eureka-6DB33F?style=flat-square&logo=spring&logoColor=white) |

---

## 📁 Galaxie des Répertoires

| Répertoire | Rôle dans l'écosystème | État |
| :--- | :--- | :--- |
| [**campushub-deployment**](https://github.com/campushub-org/campushub-deployment) | Orchestration Docker Compose, K8s et déploiement global. | 🚀 Actif |
| [**campushub-front-new**](https://github.com/campushub-org/campushub-front-new) | Interface utilisateur SaaS Next-Gen (React/TS). | ✨ Moderne |
| [**campushub-user-service**](https://github.com/campushub-org/campushub-user-service) | Service d'identité, JWT, Profils et RBAC. | 🛡️ Stable |
| [**campushub-support-service**](https://github.com/campushub-org/campushub-support-service) | Gestion du matériel pédagogique et workflow de validation. | 📚 Actif |
| [**campushub-notification-service**](https://github.com/campushub-org/campushub-notification-service) | Hub temps réel (RabbitMQ + WebSockets). | 🔔 Temps Réel |
| [**campushub-gateway-service**](https://github.com/campushub-org/campushub-gateway-service) | Passerelle d'entrée unifiée et routage dynamique. | 🚪 Connecté |
| [**campushub-cloud-config**](https://github.com/campushub-org/campushub-cloud-config) | Centralisation des configurations `.properties`. | ⚙️ Configuré |

---

## 🧬 Architecture Globale

CampusHub utilise un pattern de **Microservices asynchrones** :
1. **Routage** : Toutes les requêtes passent par l'API Gateway.
2. **Authentification** : Chaque service valide les requêtes via un secret JWT partagé.
3. **Communication** : Les services métier (Java) publient des événements sur RabbitMQ.
4. **Temps Réel** : Le service de notification (Node.js) capte les événements et les pousse via WebSockets vers le Front-end.

---

## 🚀 Démarrage Rapide

Pour tester l'ensemble de l'écosystème sur votre machine locale :

```bash
# 1. Cloner le dépôt de déploiement
git clone https://github.com/campushub-org/campushub-deployment.git
cd campushub-deployment

# 2. Compiler les services Java (Crucial)
./mvnw clean package -DskipTests

# 3. Lancer l'infrastructure complète
docker compose up -d --build
```

---

## 👨‍💻 Contribution & Contact

Nous construisons CampusHub pour la communauté académique. Si vous souhaitez contribuer ou signaler un bug, n'hésitez pas à ouvrir une Issue ou une Pull Request sur le dépôt concerné.

**Contact Technique :**  
📧 [achillefotso43@gmail.com](mailto:achillefotso43@gmail.com)  
🌐 [CampusHub Organization](https://github.com/campushub-org)

---
<p align="center">
  Développé avec passion pour l'éducation de demain. <br>
  <b>CampusHub Équipe</b> • 2024
</p>
