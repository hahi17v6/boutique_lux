# TORNADO — RAPPORT DE DÉPLOIEMENT DU THÈME SHOPIFY (PHASE 1)

---

## 1. ARBORESCENCE FINALE DU THÈME SHOPIFY OS 2.0

```
shopify-theme/
├── assets/
│   ├── favicon.svg                   # Favicon SVG 32x32px
│   ├── logo-tornado-combined.svg     # Logo combiné (Wordmark + Vortex)
│   ├── logo-vortex-symbol.svg        # Symbole Vortex seul
│   ├── tornado-tokens.css            # Design tokens (Couleurs, Typo, Radii)
│   ├── tornado-theme.css             # Styles globaux, Grille, Bento & PDP
│   └── tornado-theme.js              # JavaScript natif (Panier AJAX, Drawer, PDP)
├── config/
│   ├── settings_schema.json          # Schema d'options du Customizer Shopify
│   └── settings_data.json            # Valeurs de configuration par défaut
├── layout/
│   └── theme.liquid                  # Layout principal HTML5 / Liquid
├── locales/
│   ├── fr.json                       # Traductions Françaises
│   └── en.json                       # Traductions Anglaises
├── sections/
│   ├── header.liquid                 # En-tête avec logo, navigation, panier
│   ├── footer.liquid                 # Pied de page & réassurance
│   ├── hero-banner.liquid            # Bannière d'accueil d'impact
│   ├── bento-categories.liquid       # Grille Bento de mise en avant
│   ├── featured-collection.liquid    # Carrousel / Grille de produits en vedette
│   ├── drop-countdown.liquid         # Bannière compte à rebours drop exclusif
│   ├── newsletter-storm.liquid       # Inscription VIP newsletter Join The Storm
│   ├── main-product.liquid           # Fiche produit complète PDP
│   ├── main-collection.liquid        # Page liste de produits PLP
│   ├── main-cart-drawer.liquid       # Panier coulissant AJAX
│   ├── main-search.liquid            # Page de recherche
│   ├── main-page.liquid              # Page de contenu éditorial
│   └── main-404.liquid               # Page d'erreur 404
├── snippets/
│   ├── icon-vortex.liquid            # Icône SVG Vortex
│   ├── icon-bag.liquid               # Icône SVG Panier
│   ├── icon-search.liquid            # Icône SVG Recherche
│   ├── icon-heart.liquid             # Icône SVG Favoris
│   ├── icon-menu.liquid              # Icône SVG Burger Mobile
│   ├── icon-close.liquid             # Icône SVG Fermeture
│   ├── product-card.liquid           # Composant Carte Produit réutilisable
│   ├── price-display.liquid          # Composant d'affichage des prix & promos
│   ├── meta-tags.liquid              # Balises Open Graph & Twitter SEO
│   └── structured-data.liquid        # Données structurées JSON-LD
└── templates/
    ├── index.json                    # Template Page d'accueil OS 2.0
    ├── product.json                  # Template Fiche Produit
    ├── collection.json               # Template Collection
    ├── cart.json                     # Template Panier
    ├── search.json                   # Template Recherche
    ├── page.json                     # Template Page standard
    ├── page.contact.json             # Template Page Contact
    ├── page.faq.json                 # Template Page FAQ
    └── 404.json                      # Template Page 404
```

---

## 2. LISTE DES FICHIERS CRÉÉS ET MODIFIÉS

* **Assets & Design System :** `assets/tornado-tokens.css`, `assets/tornado-theme.css`, `assets/tornado-theme.js`, `assets/logo-tornado-combined.svg`, `assets/logo-vortex-symbol.svg`, `assets/favicon.svg`.
* **Config & Locales :** `config/settings_schema.json`, `config/settings_data.json`, `locales/fr.json`, `locales/en.json`.
* **Layout & Snippets :** `layout/theme.liquid`, `snippets/product-card.liquid`, `snippets/price-display.liquid`, `snippets/meta-tags.liquid`, `snippets/structured-data.liquid`, `snippets/icon-*.liquid`.
* **Sections (Liquid + JSON Schemas) :** 13 sections configurables via le Shopify Theme Editor.
* **Templates JSON OS 2.0 :** 9 fichiers de templates dynamiques.
* **Archive ZIP installable :** [`tornado-shopify-theme.zip`](file:///home/hahi17/Bureau/TORNADO/tornado-shopify-theme.zip).

---

## 3. DÉPENDANCES ET JUSTIFICATION

* **Aucune dépendance lourde externe.**
* Utilisation exclusive de **JavaScript Vanilla** et **Liquid natif Shopify**.
* Police typographique externe : Google Fonts (`Syne` et `Inter`) chargées en asynchrone (`preconnect` + `swap`).
* *Justification :* Garantir un score Google Lighthouse > 90/100 sur mobile et minimiser le temps de chargement sous 1,8s.

---

## 4. FONCTIONNALITÉS RÉELLEMENT TERMINÉES

* Thème 100 % compatible avec **Shopify Online Store 2.0**.
* **Panier Latéral AJAX Drawer :** Ouverture sans rechargement de page, calcul de jauge de livraison gratuite dynamique (seuil 150 €).
* **Fiche Produit (PDP) :** Sélecteur de variante/taille dynamique mis à jour en direct via `/cart/add.js`.
* **Customizer Shopify (Theme Editor) :** Réglages des textes, images, couleurs, seuil de livraison et liens sociaux configurables par l'administrateur sans toucher au code.
* **Architecture SEO & Données Structurées :** Métadonnées OpenGraph et JSON-LD `Product` et `Organization` intégrées nativement.
* **Design System Luxe :** Intégration stricte de la charte (Noir Obsidian, Blanc, Or Champagne).

---

## 5. ÉLÉMENTS SIMULÉS

* **Aucun faux backend ni fausse base de données.** Tous les objets (`product`, `collection`, `cart`, `search`) sont ceux fournis par l'API Liquid native de Shopify.
* *Note sur le développement local :* Les données présentées hors-Shopify utilisent le fallback Liquid natif pour afficher un aperçu structuré lors des tests.

---

## 6. PROBLÈMES RENCONTRÉS ET CORRIGÉS

1. **Erreur d'import de script Python :** Corrigée lors de la compilation des assets CSS/JS.
2. **Décalage Viewport Mobile Safari :** Utilisation de `dvh` et min-height 85vh pour éviter le chevauchement par la barre d'adresse iOS.
3. **Accessibilité des boutons d'icônes :** Ajout des attributs `aria-label` explicites sur l'ensemble des boutons de panier, fermeture et favoris.

---

## 7. RISQUES RESTANTS

* **Logistique & Délais Dropshipping :** Les délais de livraison devront être renseignés avec précision dans le Theme Editor pour rassurer le consommateur.
* **Optimisation des Images Uploader par le Client :** Nécessite de conseiller au marchand de télécharger des images produit au ratio 3:4 calibrées à 1200x1600px.

---

## 8. INSTRUCTIONS EXACTES POUR IMPORTER LE THÈME DANS SHOPIFY

1. Connectez-vous à votre administration Shopify (**https://admin.shopify.com**).
2. Rendez-vous dans **Boutique en ligne > Thèmes**.
3. Dans la section *Bibliothèque de thèmes*, cliquez sur **Ajouter un thème > Importer le fichier ZIP**.
4. Sélectionnez le fichier archive local : [`/home/hahi17/Bureau/TORNADO/tornado-shopify-theme.zip`](file:///home/hahi17/Bureau/TORNADO/tornado-shopify-theme.zip).
5. Cliquez sur **Téléverser le fichier**.
6. Cliquez sur **Personnaliser** pour ouvrir le Shopify Theme Editor et configurer vos collections et bannières.
7. Cliquez sur **Publier** lorsque vous souhaitez rendre le thème actif.

---

## 9. CHECKLIST DE VALIDATION

- [x] Architecture Shopify OS 2.0 propre et conforme
- [x] Thème réellement installable via archive ZIP
- [x] Aucune dépendance à un faux backend
- [x] Shopify est la source unique de vérité
- [x] Structure entièrement modulaire et évolutive
- [x] Responsive Mobile-First & Desktop ultra-rapide
- [x] Design System Luxe (Noir / Blanc / Or Champagne)
- [x] Shopify Theme Editor (Customizer) exploitable avec schemas JSON
- [x] Produits, collections, recherche et panier nativement prévus
- [x] Sécurité, SEO technique & Accessibilité (WCAG 2.1 AA) appliqués
- [x] Tests de structure effectués et validés

---

**PHASE 1 TERMINÉE — EN ATTENTE DE VALIDATION**
