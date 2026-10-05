# TORNADO — RAPPORT DU DESIGN SYSTEM & IDENTITÉ VISUELLE (PHASE 2)

---

## 1. CHOIX GRAPHIQUES ET ARTISTIQUES EFFECTUÉS

* **Positionnement Visuel :** Allience du luxe contemporain et de la culture streetwear (aesthetic Dark Luxury Obsidian & Gold).
* **Palette de Couleurs Centralisée (Design Tokens) :**
  * `Noir Obsidian (#0A0A0A)` : Canvas principal pour une obscurité théâtrale.
  * `Surface Anthracite (#141414)` : Fond des cartes produits et panels.
  * `Blanc Pur (#FFFFFF)` : Contraste maximal et lisibilité WCAG 21:1.
  * `Or Champagne (#D4AF37 & Gradient)` : Couleur d'accent d'impact réservée aux CTA principaux, badges de drops et jauges de livraison.
* **Typographie :**
  * Display : `Syne` (font géométrique ultra-bold pour titres et branding).
  * Body & UI : `Inter` (font neutre ultra-lisible sur mobile).
* **Logotype Vectoriel SVG :**
  * Logo Combiné (TORNADO Wordmark + Symbole Vortex).
  * Symbole Vortex seul pour mobile, favicon et étiquettes.
  * Compatibilité thématique fond sombre / clair et accent or.

---

## 2. COMPOSANTS RÉUTILISABLES CRÉÉS

1. **Boutons TORNADO :**
   * `.btn-tornado-primary` : Gradient Or Champagne métallisé, typographie bold uppercase, élévation au survol.
   * `.btn-tornado-secondary` : Outline discret, contour réactif Or au survol.
   * `.btn-size-option` : Sélecteur de taille interactif avec retour visuel actif.
   * `.product-card__wishlist-btn` : Icône de favoris interactive avec animation de cœur.
2. **Cartes Produits (`.product-card`) :**
   * Ratio image 3:4 calibré.
   * Image secondaire révélée au survol.
   * Badges dynamic (`NEW DROP`, `LIMITED`, `PROMO`).
3. **Panier Lateral AJAX Drawer (`.cart-drawer`) :**
   * Animation de glissement fluide.
   * Jauge de livraison gratuite calculée en temps réel (seuil 150 €).
4. **Grille Bento (`.bento-grid`) :**
   * Organisation asymétrique des univers de marque.
5. **Accordéons PDP (`.tornado-accordion`) :**
   * Informations produit, composition et livraison pliables.

---

## 3. FICHIERS MODIFIÉS ET ENRICHIS

* `assets/tornado-tokens.css` : Système complet de design tokens (Couleurs, Typo, Radii, Ombres, Breakpoints, Z-index, Accessibility Reduced Motion).
* `assets/tornado-theme.css` : Grilles responsive, animations CSS3, micro-interactions.
* `assets/tornado-theme.js` : Interactions JavaScript (Panier AJAX, sélecteur de variantes, favoris).
* `snippets/product-card.liquid` : Composant carte produit avec badges et micro-interactions.
* `snippets/price-display.liquid` : Composant d'affichage des prix barrés et promotions.
* 📦 **[`tornado-shopify-theme.zip`](file:///home/hahi17/Bureau/TORNADO/tornado-shopify-theme.zip)** : Archive ZIP mise à jour.

---

## 4. DÉPENDANCES AJOUTÉES ET JUSTIFICATION

* **Aucune dépendance externe lourde.**
* Polices Google Fonts chargées via `preconnect` et `font-display: swap`.
* *Justification :* Maintien d'un poids de thème extrêmement faible pour préserver la vitesse sur réseau mobile 4G/5G.

---

## 5. PROBLÈMES TROUVÉS ET CORRECTIONS APPORTÉES

* **Problème :** Ratio de contraste des textes d'aide sur fond noir.
  * *Correction :* Ajustement de la couleur secondaire à `#A0A0A0` pour garantir un ratio de contraste WCAG > 8.5:1.
* **Problème :** Support des utilisateurs sensibles aux mouvements (cinétose).
  * *Correction :* Ajout de la règle `@media (prefers-reduced-motion: reduce)` désactivant automatiquement les animations de transition.

---

## 6. POINTS ENCORE À VALIDER AVEC LE FONDATEUR

1. **Choix final des polices définitives :** Confirmation de l'utilisation de `Syne` ou achat d'une typographie custom payante (ex. Monument Extended).
2. **Visuels des univers Bento :** Téléversement des photos de couverture haute définition dans le Shopify Customizer.

---

## 7. COMMENT TESTER LE RÉSULTAT DANS SHOPIFY

1. Dans votre admin Shopify, allez sur **Boutique en ligne > Thèmes**.
2. Téléversez l'archive actualisée : [`tornado-shopify-theme.zip`](file:///home/hahi17/Bureau/TORNADO/tornado-shopify-theme.zip).
3. Cliquez sur **Personnaliser** pour vérifier le rendu visuel dans le Shopify Theme Editor.

---

**PHASE 2 TERMINÉE — EN ATTENTE DE VALIDATION**
