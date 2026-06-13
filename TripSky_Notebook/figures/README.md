# Figures — TripSky Analysis

Toutes les figures sont exportées en PNG (100 DPI) depuis le notebook principal.

| # | Fichier | Section notebook | Description |
|---|---------|-----------------|-------------|
| 01 | `01_revenu_par_destination.png` | §4.1 | Revenu total par destination — 12 destinations classées |
| 02 | `02_revenu_par_type.png` | §4.2 | Revenu et panier moyen par type de voyage (Culturel / Aventure / Détente) |
| 03 | `03_saison.png` | §4.3 | Revenu par saison — Été 53,7% au-dessus du Printemps |
| 04 | `04_age.png` | §4.4 | Distribution du revenu par tranche d'âge client |
| 05 | `05_evaluations.png` | §4.5 | Distribution des évaluations — 51,6% de notes ≤ 2/5 |
| 06 | `06_paiement.png` | §4.6 | Répartition des modes de paiement (Virement / PayPal / Carte) |
| 07 | `07_revenu_pub_mensuel.png` | §4.7 | Revenu mensuel vs dépenses pub — Jan 2023 → Mar 2025 |
| 08 | `08_correlation_pub_revenu.png` | §4.8 | Corrélation pub ↔ revenu journalier (r = -0,036) |
| 09 | `09_jour_semaine.png` | §4.9 | Volume de réservations par jour de la semaine |
| 10 | `10_heatmap_recommandation.png` | §5 | Heatmap priorité : destination × saison (recommandation finale) |

## Lecture de la heatmap (figure 10)
Les cellules les plus foncées = segments à **cibler en priorité**.
- **Axe X** : saison de voyage
- **Axe Y** : destination
- **Valeur** : revenu total du segment

> Segments prioritaires : Népal/Été, Bali/Été, France/Hiver
