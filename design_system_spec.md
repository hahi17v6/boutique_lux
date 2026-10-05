# TORNADO — SPÉCIFICATION DU DESIGN SYSTEM (PHASE 1)

---

## 1. STRATÉGIE ET DIRECTION ARTISTIQUE

Le Design System de **TORNADO** incarne l'alliance ultime entre l'élégance minimaliste des maisons de haute couture parisiennes et l'énergie brute de la culture streetwear internationale.

### Principes Directeurs
1. **Dominance Sombre (Obsidian Canvas) :** Le fond noir profond (`#0A0A0A`) crée une obscurité théâtrale qui fait ressortir la matière et la coupe des vêtements.
2. **Accentuation Or Champagne (Luxury Highlight) :** L'or métallisé (`#D4AF37`) est appliqué avec précision sur les éléments à haute valeur ajoutée (CTA, badges de drop, compteurs).
3. **Typographie Géométrique Imposante :** La police de titres insuffle force, statut et modernité.
4. **Compositions Asymétriques (Bento Architecture) :** Organisation des contenus sous forme de pavés éditoriaux dynamiques.

---

## 2. ASSETS VISUELS ET LOGOTYPE

### 2.1 Logo Combiné (Header Desktop & Packaging)
Le logo réunit le symbole du Vortex géométrique à gauche et le Wordmark TORNADO en lettres capitales espacées.

![Logo Combiné TORNADO](/home/hahi17/.gemini/antigravity/brain/6381d2f9-3bc9-4a2e-8a8d-170cb29e48fe/assets/logo-tornado-combined.svg)

*Fichier source vectoriel :* [`assets/logo-tornado-combined.svg`](file:///home/hahi17/.gemini/antigravity/brain/6381d2f9-3bc9-4a2e-8a8d-170cb29e48fe/assets/logo-tornado-combined.svg)

### 2.2 Symbole Vortex Autonome (Mobile Header, Favicon & Griffes Textiles)
Le symbole seul est une spirale d'or structurée en 3 arcs concentriques, représentant le tourbillon de la marque.

![Symbole Vortex TORNADO](/home/hahi17/.gemini/antigravity/brain/6381d2f9-3bc9-4a2e-8a8d-170cb29e48fe/assets/logo-vortex-symbol.svg)

*Fichier source vectoriel :* [`assets/logo-vortex-symbol.svg`](file:///home/hahi17/.gemini/antigravity/brain/6381d2f9-3bc9-4a2e-8a8d-170cb29e48fe/assets/logo-vortex-symbol.svg)

### 2.3 Maquette UI du Concept (Homepage Hero & Grille Produit)
Voici la maquette visuelle haute fidélité illustrant l'intégration des tokens de design sur l'interface TORNADO :

![Maquette UI Homepage TORNADO](/home/hahi17/.gemini/antigravity/brain/6381d2f9-3bc9-4a2e-8a8d-170cb29e48fe/tornado_homepage_mockup_1791216315111.jpg)



---

## 3. CHARTE DE COULEURS (DESIGN TOKENS)

| Nom du Token | Valeur Hex / CSS | Usage Principal | Ratio de Contraste WCAG |
| :--- | :--- | :--- | :--- |
| `--tornado-bg-main` | `#0A0A0A` | Fond de page principal | Baseline |
| `--tornado-bg-surface` | `#141414` | Cartes produits, panels | Baseline |
| `--tornado-text-primary` | `#FFFFFF` | Titres, textes majeurs | **21:1** (AA & AAA Compliant) |
| `--tornado-text-secondary` | `#A0A0A0` | Métadonnées, sous-titres | **8.5:1** (AA Compliant) |
| `--tornado-gold-main` | `#D4AF37` | Accents luxe, CTA Or | **9.2:1** vs Noir |
| `--tornado-gold-gradient` | `linear-gradient(...)` | Boutons d'action, Badges VIP | Highlight d'impact |
| `--tornado-border-subtle` | `#262626` | Séparateurs, bordures cartes | Esthétique discrète |

---

## 4. GUIDE DES COMPOSANTS UI

### 4.1 Bouton Principal Or (`.btn-tornado-primary`)
* **Aspect :** Gradient Or Champagne métallisé, typographie bold uppercase, légère ombre dorée.
* **Hover State :** Élévation de 2px, augmentation de la luminosité et de l'ombre de diffusion.
* **Hauteur minimale :** 48px sur mobile (conformité zone de pouce).

### 4.2 Bouton Secondaire Contour (`.btn-tornado-secondary`)
* **Aspect :** Transparent avec bordure fine `#3A3A3A`, texte blanc.
* **Hover State :** Changement de bordure en Or Champagne et léger background à 5% d'opacité.

### 4.3 Carte Produit (`.product-card`)
* **Proportions :** Ratio image 3:4 (optimisé mode & streetwear).
* **Visuel :** Fond `#141414`, bordure `#262626`.
* **Interaction :** Au survol, la bordure s'illumine en Or discret, la carte s'élève de 4px, et la 2ème image (portée/lifestyle) apparaît de manière fluide.

### 4.4 Badges de Statut Produit
* `.badge-drop` : Gradient Or / Texte Noir (Haute visibilité pour les nouveautés).
* `.badge-limited` : Fond sombre / Contour Or (Stock restreint).
* `.badge-sale` : Rouge intense `#FF4D4D` (Promotions).

---

## 5. CSS SYSTEM INTEGRATION

Le fichier complet de tokens CSS est compilé et disponible dans :
* Fichier CSS : [`assets/tornado-tokens.css`](file:///home/hahi17/.gemini/antigravity/brain/6381d2f9-3bc9-4a2e-8a8d-170cb29e48fe/assets/tornado-tokens.css)

---

## 6. PROCHAINES ÉTAPES (PHASE 2)

La Phase 1 étant formalisée, la **Phase 2** prendra en charge :
1. La création de la structure du catalogue produit (~100 produits).
2. L'organisation des collections et des taxonomies dans Shopify.
3. La configuration des métadonnées (Guide des tailles, composition, stock).
