# 📱 Prédiction du Churn Client dans les Services Mobile Money

## 📖 Contexte

Dans un environnement fortement concurrentiel, la fidélisation des clients constitue un enjeu majeur pour les opérateurs de services Mobile Money. La capacité à identifier les utilisateurs susceptibles de quitter le service permet de mettre en place des actions préventives et d'améliorer la rétention.

Ce projet de Data Science vise à développer un modèle de prédiction du churn à partir de données transactionnelles Mobile Money et à proposer une interface interactive facilitant l'analyse des comportements clients.

---

## 🎯 Objectifs

* Analyser les comportements transactionnels des utilisateurs.
* Identifier les facteurs influençant le churn.
* Construire un modèle de Machine Learning capable de prédire les risques d'attrition.
* Développer un dashboard interactif permettant l'exploration des données et la prédiction en temps réel.

---

## 📊 Description des données

Le jeu de données contient plus de 900 000 transactions Mobile Money enregistrées sur une période de plusieurs jours.

### Variables principales

| Variable        | Description                                         |
| --------------- | --------------------------------------------------- |
| channel         | Canal utilisé pour la transaction                   |
| typetransaction | Nature de l'opération effectuée                     |
| montant         | Montant de la transaction                           |
| fees            | Frais associés à l'opération                        |
| statuscode      | Statut de la transaction                            |
| date            | Date et heure de l'opération                        |
| churn           | Variable cible (1 = client perdu, 0 = client actif) |

---

## 🛠️ Technologies utilisées

* Python
* Pandas
* NumPy
* Scikit-Learn
* Plotly
* Streamlit
* Joblib

---

## 🔍 Méthodologie

### 1. Préparation des données

* Nettoyage des données
* Gestion des valeurs manquantes
* Suppression des doublons
* Traitement des valeurs aberrantes

### 2. Analyse exploratoire

* Distribution des montants
* Analyse du churn par canal
* Analyse du churn par type de transaction
* Étude des tendances temporelles

### 3. Modélisation

Deux modèles ont été évalués :

* Régression Logistique
* Random Forest

Le modèle Random Forest a présenté les meilleures performances globales et a été retenu pour l'application finale.

---

## 📈 Résultats obtenus

### Performance des modèles

| Modèle                | Accuracy | Recall Churn |
| --------------------- | -------- | ------------ |
| Régression Logistique | 45.15 %  | 60 %         |
| Random Forest         | 61.27 %  | 44 %         |

### Variables les plus influentes

1. Montant de la transaction
2. Heure de réalisation
3. Frais appliqués
4. Type de transaction
5. Canal utilisé

---

## 💻 Dashboard Interactif

L'application Streamlit permet :

* La visualisation des indicateurs clés
* L'analyse détaillée du churn
* La consultation des données filtrées
* La prédiction du risque de churn en temps réel

---

## 🚀 Installation

### Cloner le projet

```bash
git clone <url-du-projet>
```

### Installer les dépendances

```bash
pip install -r requirements.txt
```

### Lancer l'application

```bash
streamlit run dashboard.py
```

---

## 📁 Structure du projet

```text
projet_churn/
│
├── dashboard.py
├── modele_churn.pkl
├── train_om.csv
├── requirements.txt
└── README.md
```

---

## 🔮 Perspectives d'amélioration

* Intégration de XGBoost et LightGBM
* Gestion avancée du déséquilibre des classes avec SMOTE
* Déploiement Cloud
* Système d'alertes automatiques
* Suivi temps réel des indicateurs métier

---

## 👩‍💻 Auteur

Nisrine Attoumane

Master 2 – Ingénierie Mathématique et Numérique

Université Cheikh Anta Diop de Dakar (UCAD)

---

## 📄 Licence

Projet réalisé à des fins pédagogiques et académiques.
