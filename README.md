# Système de Gestion de Tickets avec Intelligence Artificielle

## Description
Ce projet est un système complet de gestion de tickets d'assistance technique intégré à Jira, utilisant l'intelligence artificielle pour classifier automatiquement les tickets et améliorer l'efficacité du support. Il comprend une interface administrateur pour la gestion des tickets, une interface utilisateur pour la soumission de demandes, et un modèle de machine learning pour la catégorisation automatique.

## Fonctionnalités Principales
- **Interface Administrateur** : Dashboard avec visualisation des KPIs, gestion des tickets, et classification automatique
- **Interface Utilisateur** : Portail de soumission de tickets avec formulaire intuitif
- **Intégration Jira** : Synchronisation bidirectionnelle avec Jira pour la gestion des tickets
- **Classification IA** : Modèle de machine learning pour catégoriser automatiquement les tickets
- **Prétraitement de Texte** : Nettoyage et préparation des données textuelles en français
- **Visualisation des Données** : Graphiques et métriques pour analyser les performances

## Structure du Projet

```
/Users/ulricheneli/Desktop/Mise En SP - Tickets/
├── interface.py                 # Interface administrateur Streamlit
├── user_interface.py            # Interface utilisateur pour soumission de tickets
├── jira_integration.py          # Scripts d'intégration avec Jira
├── jira_update.py               # Mise à jour des tickets Jira
├── model_training.py            # Entraînement du modèle de classification
├── prediction.py                # Prédiction des catégories avec le modèle
├── preprocessing.py             # Prétraitement des données textuelles
├── ticket.py                    # Classes et utilitaires pour les tickets
├── cleaned_tickets.csv          # Données prétraitées
├── tickets_annotes.csv          # Données d'entraînement annotées
├── tickets.csv                  # Données brutes des tickets
├── Interfaces/
│   ├── tickets.csv
│   ├── verif.py
│   ├── Backend/
│   ├── Data/
│   ├── env/                     # Environnement virtuel Python
│   ├── Function/
│   ├── monenv/                  # Autre environnement virtuel
│   └── Pages/
│       ├── user_interface.py
│       └── Page-Acceuil/
│           ├── connexion.html
│           ├── contact.css
│           ├── contact.html
│           ├── db.php
│           ├── login.php
│           ├── logo.csv
│           ├── readme            
│           ├── register.php
│           ├── site.css
│           ├── site.html
│           ├── style.css
│           ├── stylecon.css
│           ├── testflask.py
│           ├── ticketsystem.sql
│           ├── varcon.css
│           └── vars.css
├── Maquette figma/              # Maquettes de conception
├── Image/                       # Ressources images
├── Photo/                       # Photos du projet
├── Rendu Attendu/               # Spécifications attendues
└── ressources/                  # Ressources supplémentaires
```

## Installation

### Prérequis
- Python 3.8+
- Compte Jira avec API token
- Modèle SpaCy français (`fr_core_news_sm`)

### Étapes d'Installation

1. **Cloner le projet**
   ```bash
   git clone <url-du-repo>
   cd "Mise En SP - Tickets"
   ```

2. **Créer un environnement virtuel**
   ```bash
   python -m venv env
   source env/bin/activate  # Sur macOS/Linux
   # ou env\Scripts\activate sur Windows
   ```

3. **Installer les dépendances**
   ```bash
   pip install -r requirements.txt
   ```

4. **Installer le modèle SpaCy**
   ```bash
   python -m spacy download fr_core_news_sm
   ```

5. **Configurer les variables d'environnement**
   Créer un fichier `.env` avec :
   ```
   JIRA_URL=https://votre-instance.atlassian.net
   JIRA_EMAIL=votre-email@jira.com
   JIRA_API_TOKEN=votre-api-token
   ```

## Utilisation

### Interface Administrateur
```bash
streamlit run interface.py
```
Accédez à `http://localhost:8501` pour le dashboard administrateur.

### Interface Utilisateur
```bash
streamlit run Interfaces/Pages/user_interface.py
```
Accédez à `http://localhost:8501` pour le portail de soumission de tickets.

### Entraînement du Modèle
```bash
python model_training.py
```

### Prédiction sur un Ticket
```bash
python prediction.py
```

## Dépendances
- streamlit
- pandas
- scikit-learn
- spacy
- jira-python
- matplotlib
- joblib
- numpy

## Configuration Jira
Le projet utilise l'API Jira pour :
- Créer des tickets depuis l'interface utilisateur
- Lire les tickets pour classification
- Mettre à jour les labels avec les catégories prédites

Assurez-vous d'avoir :
- Une instance Jira accessible
- Un compte avec permissions API
- Un token API généré

## Modèle de Machine Learning
Le système utilise un classificateur SVM entraîné sur des données de tickets annotées pour prédire automatiquement les catégories suivantes :
- Support utilisateur
- Problème matériel/logiciel
- Accès/authentification
- Et plus de 40 catégories spécialisées

## Développement Web
Le dossier `Page-Acceuil/` contient une implémentation alternative en HTML/CSS/PHP pour l'interface web, incluant :
- Page de connexion
- Système d'inscription
- Base de données MySQL
- Interface responsive

## Contribution
1. Fork le projet
2. Créer une branche feature
3. Commiter vos changements
4. Push vers la branche
5. Créer une Pull Request


## Auteur
Ulrich Eneli

## Date
14 avril 2026



