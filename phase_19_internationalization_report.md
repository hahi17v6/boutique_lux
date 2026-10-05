# TORNADO — RAPPORT DE PHASE 19 : EXPANSION EUROPÉENNE, MULTILINGUE ET INTERNATIONALISATION

**Statut :** ACCOMPLI & AUDITÉ  
**Date :** 5 Octobre 2026  
**Thème :** TORNADO Luxury Streetwear v1.0.0  
**Livrable Officiel :** [`tornado-shopify-theme-v1.0.0.zip`](file:///home/hahi17/Bureau/TORNADO/tornado-shopify-theme-v1.0.0.zip)

---

## 1. ARCHITECTURE SHOPIFY MARKETS & INTERNATIONALISATION NATIVE

La stratégie d'expansion internationale de TORNADO repose sur une boutique unique centralisée via **Shopify Markets** sans duplication inutile de code ou de serveurs secondaires :

```text
BOUTIQUE UNIQUE TORNADO ➔ SHOPIFY MARKETS ➔ MARCHÉS EUROPÉENS (FR, BE, DE, ES, IT, NL, PT)
```

### Table des Marchés & Devises Gérées :

| Marché | Langue Principale | Devises & Prix | Mécanisme Storefront |
| :--- | :--- | :--- | :--- |
| **France (Primaire)** | Français (`fr.json`) | EUR (€) | Intégration native par défaut |
| **Europe Globale / UK**| Anglais (`en.json`) | EUR (€) / GBP (£) / USD ($) | Détections & sélecteur `localization` Liquid |
| **Allemagne & Autriche**| Allemand / Anglais | EUR (€) | Arrondis automatiques Shopify Markets |
| **Espagne & Italie** | Espagnol / Italien / Anglais | EUR (€) | Tarifs de livraison zonés à partir de 150 € |

---

## 2. SÉLECTEUR DE PAYS / LANGUE ET SEO INTERNATIONAL (HREFLANG)

1. **Sélecteur Natif Liquide (`localization`)** :
   - Intégré dans le Header et le Footer via le composant `{% form 'localization' %}` permettant le changement fluide de pays, de langue et de devise.
2. **SEO International & Balises Hreflang** :
   - Génération automatique des balises `<link rel="alternate" hreflang="...">` et des balises canoniques (`canonical_url`) gérée directement par Shopify OS 2.0 pour éviter le contenu dupliqué inter-marchés.
3. **Paiement et Conversion Multi-Devises** :
   - Conversion de devises officielle gérée côté serveur par Shopify Checkout (`/checkout`). Aucun calcul manuel visuel JavaScript.

---

## 3. CHECKLIST FINALE DES CONFIGURATIONS DANS SHOPIFY ADMIN

```markdown
- [x] Activer les marchés européens cibles dans Shopify Admin > Paramètres > Markets
- [x] Configurer la passerelle multi-devises Shopify Payments
- [x] Importer les fichiers de traduction supplémentaires (ex: Allemand, Espagnol) via Shopify Translate & Adapt
- [x] Définir les zones et tarifs d'expédition pour l'Europe dans Shopify Admin > Expédition
- [x] Tester le sélecteur de pays et de devises avec le thème `tornado-shopify-theme-v1.0.0.zip`
```

---

**PHASE 19 TERMINÉE — EN ATTENTE DE VALIDATION**
