# Projet DevOps - Pipeline CI/CD Complet

## 📋 Description

Ce projet présente une implémentation complète d'un pipeline CI/CD moderne utilisant les meilleures pratiques DevOps. Il comprend une application full-stack (Spring Boot + Angular) avec une base de données MySQL, déployée à travers un pipeline Jenkins automatisé incluant tests, analyse de code, containerisation et monitoring.

## 🏗️ Architecture

### Stack Technologique
- **Backend**: Spring Boot (Java)
- **Frontend**: Angular
- **Base de données**: MySQL
- **CI/CD**: Jenkins
- **Containerisation**: Docker & Docker Compose
- **Registry**: Docker Hub, Nexus Repository Manager
- **Monitoring**: Grafana + Prometheus
- **Tests de charge**: Apache JMeter
- **Analyse de code**: SonarQube
- **Tests unitaires**: JUnit avec JaCoCo

### Composants du Pipeline

```
Code Source → Jenkins → Tests → Build → SonarQube → Docker → Deploy → Monitor
```

## 🚀 Fonctionnalités

### Pipeline CI/CD
- ✅ Déclenchement automatique sur changements de code
- ✅ Tests unitaires automatisés avec couverture >90%
- ✅ Analyse de qualité de code avec SonarQube
- ✅ Build et packaging automatiques
- ✅ Déploiement d'artefacts vers Nexus
- ✅ Création et push d'images Docker
- ✅ Déploiement automatisé avec Docker Compose
- ✅ Notifications par email
- ✅ Monitoring avec Grafana/Prometheus

### Tests et Qualité
- Tests unitaires JUnit pour le backend
- Couverture de code avec JaCoCo
- Analyse statique avec SonarQube
- Tests de charge avec JMeter

## 📦 Services et Ports

| Service | Port | Description |
|---------|------|-------------|
| Backend (Spring Boot) | 8081 | API REST |
| Frontend (Angular) | 80 | Interface utilisateur |
| MySQL | 3333 | Base de données |
| Jenkins | 9999 | Serveur CI/CD |
| Nexus | 9997 | Repository Manager |
| Grafana | 3000 | Dashboard monitoring |
| Prometheus | 9090 | Collecte de métriques |

## 🛠️ Installation et Configuration

### Prérequis
- Docker & Docker Compose
- Java 11+
- Node.js & npm
- Maven
- Git

### Étapes de déploiement

1. **Cloner le repository**
   ```bash
   git clone <repository-url>
   cd devops-cicd-project
   ```

2. **Configurer Jenkins**
   ```bash
   # Démarrer Jenkins
   docker run -d -p 9999:8080 jenkins/jenkins:lts
   ```

3. **Déployer l'infrastructure**
   ```bash
   # Démarrer tous les services
   docker-compose up -d
   ```

4. **Configurer le pipeline Jenkins**
   - Créer un nouveau job Pipeline
   - Lier au repository Git
   - Configurer les webhooks

## 📊 Monitoring et Métriques

### Grafana Dashboards
- Métriques d'application
- Utilisation des ressources
- Performance de la base de données
- Métriques du pipeline CI/CD

### Prometheus Targets
- Application metrics
- System metrics
- Database metrics
- Jenkins metrics

## 🧪 Tests de Charge

### Configuration JMeter
- **Utilisateurs simulés**: 50
- **Période de montée en charge**: 10 secondes
- **Nombre d'itérations**: 10
- **Endpoints testés**: API de gestion des tâches

### Scenarios de test
- Création de tâches
- Mise à jour de tâches
- Suppression de tâches
- Tests de stress et endurance

## 📁 Structure du Projet

```
├── backend/                 # Application Spring Boot
│   ├── src/
│   ├── pom.xml
│   └── Dockerfile
├── frontend/               # Application Angular
│   ├── src/
│   ├── package.json
│   └── Dockerfile
├── docker-compose.yml      # Configuration des services
├── Jenkinsfile            # Pipeline CI/CD
├── monitoring/            # Configuration Grafana/Prometheus
├── jmeter/               # Scripts de tests de charge
└── README.md
```

## 🔧 Configuration

### Variables d'environnement
- `DB_HOST`: Hôte de la base de données
- `DB_PORT`: Port de la base de données
- `DB_NAME`: Nom de la base de données
- `DB_USER`: Utilisateur de la base de données
- `DB_PASSWORD`: Mot de passe de la base de données

### Credentials Jenkins
- Docker Hub credentials
- Nexus credentials
- Email server settings
- SonarQube token

## 📈 Métriques de Qualité

### Objectifs
- **Couverture de code**: >90%
- **Qualité SonarQube**: Grade A
- **Temps de build**: <10 minutes
- **Temps de déploiement**: <5 minutes

## 🚨 Alertes et Notifications

### Email Notifications
- Succès/échec du build
- Déploiement réussi
- Erreurs critiques

### Alertes Prometheus
- Utilisation CPU > 80%
- Utilisation mémoire > 90%
- Erreurs d'application > 5%

## 🤝 Contribution

1. Fork le projet
2. Créer une branche feature (`git checkout -b feature/AmazingFeature`)
3. Commit les changements (`git commit -m 'Add AmazingFeature'`)
4. Push vers la branche (`git push origin feature/AmazingFeature`)
5. Ouvrir une Pull Request
