# TripSky — Analyse des ventes et recommandation marketing

Analyse complète des données de ventes de TripSky (agence de voyages insolites)
pour identifier les segments à fort potentiel et optimiser le budget marketing.

## Contexte
- **798 clients** analysés sur **800 jours** (Jan 2023 – Mar 2025)
- **Revenu total** : 3 966 171 €
- **Problème** : ROI publicitaire négatif (-1,13%) — où concentrer le budget ?

## Stack
- Python 3.x · pandas · matplotlib · seaborn
- Jupyter Notebook
- PowerPoint / Word pour les livrables

## Structure
```
TripSky_Notebook/        → Jupyter notebook + figures exportées + insights.json
TripSky_Rapport.docx     → Rapport d'analyse complet
TripSky-Analysis.pptx    → Présentation exécutive
```

## Résultats clés
- 🥇 Destination top : **Népal** (422 498 €)
- 🌞 Saison top : **Été** (53,7% de plus que le Printemps)
- ⚠️  Note moyenne : **2,48/5** — 51,6% de notes basses
- 💡 Économie potentielle : **152 708 €/an** en réallouant le budget pub

## Livrables
- 📓 `TripSky_Notebook/TripSky_Analyse.ipynb` — notebook complet reproductible
- 📊 `TripSky_Notebook/figures/` — 10 visualisations exportées
- 📄 `TripSky_Rapport.docx` — rapport d'analyse complet
- 📑 `TripSky-Analysis.pptx` — présentation exécutive
- 🔢 `TripSky_Notebook/insights.json` — KPIs exportés en JSON

## Quick Start
```bash
pip install -r requirements.txt
jupyter notebook TripSky_Notebook/TripSky_Analyse.ipynb
```
