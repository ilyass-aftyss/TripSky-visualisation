# Changelog — TripSky Analysis

## v1.0.0 — 13 juin 2026

### Ajouté
- Notebook d'analyse complet (8 sections, 9 visualisations + heatmap recommandation)
- Export `insights.json` avec 20+ KPIs calculés automatiquement
- 10 figures PNG haute résolution exportées dans `TripSky_Notebook/figures/`
- Rapport Word complet (`TripSky_Rapport.docx`)
- Présentation PowerPoint exécutive (`TripSky-Analysis.pptx`)
- Recommandations chiffrées avec matrice de priorité
- Dictionnaire de données (`DATA_DICTIONARY.md`)
- Méthodologie documentée (`METHODOLOGY.md`)
- Synthèse des insights (`insights_summary.md`)
- Guide de lecture des figures (`TripSky_Notebook/figures/README.md`)

### Données nettoyées
- 798 clients propres (sur 801 bruts)
- 3 outliers d'âge corrigés (220, 350, 4100 → NaN)
- Doublons supprimés
- Casse des catégories normalisée (Title case)

### Résultats clés
- ROI pub : -1,13% → budget à réallouer
- Économie potentielle : 152 708 €/an
- Uplift revenu potentiel : +122 941 €/an
- Segments focus : Été × Népal / Bali / France
