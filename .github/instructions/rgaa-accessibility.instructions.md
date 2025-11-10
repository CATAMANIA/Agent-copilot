---
applyTo: "**/*.html, **/*.tsx, **/*.jsx, **/*.vue, **/*.ts, **/*.js, **/*.css, **/*.scss"
---

# Standards d'accessibilité RGAA 4.1

Cette instruction couvre les règles d'accessibilité RGAA 4.1 pour garantir la conformité aux standards d'accessibilité français et européens.

## Vue d'ensemble RGAA 4.1

Le Référentiel Général d'Amélioration de l'Accessibilité (RGAA) 4.1 est basé sur les WCAG 2.1 et définit 106 critères répartis en 13 thématiques.

### Niveaux de conformité
- **Niveau A** : Critères de base (25 critères)
- **Niveau AA** : Critères avancés (50 critères) - **OBLIGATOIRE pour les services publics**
- **Niveau AAA** : Critères experts (31 critères) - Recommandé

## 13 Thématiques RGAA 4.1

### 1. Images (8 critères)

#### Textes alternatifs obligatoires
```html
<!-- ✅ BON - Image informative avec alt descriptif -->
<img src="graphique-ventes.png" alt="Graphique des ventes en hausse de 15% en 2024" />

<!-- ✅ BON - Image décorative avec alt vide -->
<img src="decoration.png" alt="" role="presentation" />

<!-- ❌ MAUVAIS - Alt manquant -->
<img src="important-graph.png" />
```