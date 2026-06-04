# Méthodologie — TripSky Analysis

## 1. Source des données
- `clients_TripSky.csv` — 801 lignes brutes, 16 colonnes comportementales
- `entreprise_TripSky.csv` — 800 jours d'activité (Jan 2023 – Mar 2025)

## 2. Nettoyage appliqué

| Problème détecté | Action |
|-----------------|--------|
| 3 doublons exacts | Supprimés (`drop_duplicates()`) |
| 3 doublons d'ID_Client | Conservé le premier (`keep='first'`) |
| 3 outliers d'âge (220, 350, 4100) | Remplacés par NaN |
| Casse incohérente (culturel/Culturel) | `.str.strip().str.title()` |
| 164 genres manquants | Conservés NaN (non imputés — biais potentiel) |
| 152 modes de paiement manquants | Conservés NaN |
| 5 destinations manquantes | Conservés NaN |

**Résultat :** 798 lignes propres sur 801 brutes.

## 3. Variables dérivées
- `tranche_age` : tranches [18-25, 26-35, 36-45, 46-55, 55+]
- `prix_par_personne` : prix total / nombre de personnes

## 4. Analyses réalisées

| # | Analyse | Fichier figure |
|---|---------|---------------|
| 4.1 | Revenu par destination (12 dest.) | `01_revenu_par_destination.png` |
| 4.2 | Panier moyen par type de voyage | `02_revenu_par_type.png` |
| 4.3 | Saisonnalité (4 saisons) | `03_saison.png` |
| 4.4 | Revenu par tranche d'âge | `04_age.png` |
| 4.5 | Distribution des évaluations | `05_evaluations.png` |
| 4.6 | Modes de paiement | `06_paiement.png` |
| 4.7 | Revenu mensuel vs pub (série temp.) | `07_revenu_pub_mensuel.png` |
| 4.8 | Corrélation pub ↔ revenu (scatter) | `08_correlation_pub_revenu.png` |
| 4.9 | Réservations par jour de semaine | `09_jour_semaine.png` |
| 5 | Heatmap destination × saison | `10_heatmap_recommandation.png` |

## 5. Limites de l'analyse
- Données publicitaires sans segmentation par canal (SEA, social, display)
- Pas de données de coût par type de voyage → panier ≠ marge réelle
- Période courte (2 ans) — tendances saisonnières à confirmer sur 3+ ans
- 20% de genre manquant → segmentation démographique partielle

## 6. Reproductibilité
```bash
pip install -r requirements.txt
jupyter notebook TripSky_Notebook/TripSky_Analyse.ipynb
```
Les fichiers CSV doivent être placés dans `attached_assets/` avec les noms originaux.
