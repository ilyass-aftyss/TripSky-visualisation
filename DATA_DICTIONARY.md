# Dictionnaire des données — TripSky

## Fichier clients (800 lignes, 16 colonnes)

| Colonne | Type | Description |
|---------|------|-------------|
| ID_Client | int | Identifiant unique client |
| âge | int | Âge du client (3 outliers corrigés : 220, 350, 4100 → NaN) |
| genre | str | M / F / Autre (164 valeurs manquantes) |
| type de voyage | str | Culturel / Aventure / Détente (normalisé en Title case) |
| destination | str | 12 destinations (Bali, Népal, France, Norvège, Costa Rica…) |
| saison de voyage | str | Été / Hiver / Automne / Printemps |
| durée de voyage (en jours) | int | 5 à 19 jours (moy. 9,6 j) |
| nombre de personnes | int | 1 à 5 personnes (moy. 2,9) |
| prix total | int | Revenu de la réservation en € (105 → 11 254) |
| mode de paiement | str | Virement / PayPal / Carte de crédit |
| évaluation sur 5 | int | 1 à 5 (moy. 2,48 — très bas) |
| date de début de voyage | str | Format DD-MM-YYYY |
| date de fin de voyage | str | Format DD-MM-YYYY |
| période de voyage | str | Concaténation début → fin |
| budget_voyage_annuel | int | Budget annuel déclaré en € (618 → 8 903) |
| durée moyenne de voyage annuelle (en jours) | float | Moy. 15 jours/an |

## Fichier entreprise (800 jours, Jan 2023 – Mar 2025)

Données quotidiennes agrégées de l'activité de l'entreprise.

| Colonne | Description |
|---------|-------------|
| Date | Date au format DD/MM/YY |
| Réservations | Nombre de réservations du jour |
| Revenu | Revenu journalier en € |
| Dépenses publicitaires | Budget pub dépensé ce jour en € |

## Variables dérivées (créées dans le notebook)

| Variable | Calcul | Usage |
|----------|--------|-------|
| tranche_age | `pd.cut(âge, [0,25,35,45,55,100])` | Segmentation démographique |
| prix_par_personne | `prix total / nombre de personnes` | Panier unitaire |
