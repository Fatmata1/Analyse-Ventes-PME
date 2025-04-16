# Analyse-Ventes-PME# Analyse des Ventes d’une PME – Projet Data Engineer

## Objectif du Projet

Ce projet consiste à construire une solution automatisée pour :
- Créer une base de données `ventes_pme.db`
- Importer automatiquement des données de ventes, produits et magasins (CSV)
- Effectuer des analyses SQL pour répondre à des questions stratégiques :
  - Chiffre d'affaires total
  - Ventes par produit
  - Ventes par région
- Stocker les résultats des analyses dans une table dédiée : `résultats_analyse`

## Technologies utilisées

- Python 3
- SQLite (via `sqlite3`)
- Pandas
- Docker & Docker Compose

## Structure du Projet

```
projet-analyse-ventes/
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
├── main.py
├── data/                 # Contient la base ventes_pme.db
├── produits.csv
├── ventes.csv
└── magasins.csv
```

## Lancement du Projet

1. Assurez-vous que Docker et Docker Compose sont installés
2. Placez-vous dans le dossier du projet
3. Lancez les conteneurs :

```docker-compose down : delete all existing containers


docker-compose up --build
```

4. La base de données `ventes_pme.db` sera créée.
5. Les résultats seront visibles dans la table `résultats_analyse`

## Résultats stockés

La table `résultats_analyse` contient :
- La date d’analyse (`date_analyse`)
- Le nom de l’indicateur (`indicateur`)
- La valeur (chiffre ou JSON) (`valeur`)

Exemples :
- `chiffre_affaires_total`
- `ventes_par_produit`
- `ventes_par_region`

## Démonstration

La démonstration vidéo montre :
- Le lancement automatisé de la solution via Docker
- Les logs d’import et d’analyse
- L’état final de la base dans DB Browser for SQLite

---

