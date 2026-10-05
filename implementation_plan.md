# Plan d'Implémentation — Phase 1 : Direction Artistique, Branding & Design System

La Phase 0 ayant été validée, la **Phase 1** établit les fondations visuelles et la charte graphique de la marque **TORNADO**.

---

## 1. Objectifs de la Phase 1

1. **Création du Logo & Symbole Vortex :** Générer les assets vectoriels SVG (Logo combiné, Wordmark seul, Symbole Vortex seul, Favicon).
2. **Design System & Tokens CSS :** Établir le fichier de variables CSS (`tornado-tokens.css`) contenant la palette (Noir Obsidian, Blanc Pur, Or Champagne Métallisé), les typographies, les espacements, et les ombres.
3. **Mockups UI & Layouts :** Définir la maquette visuelle et l'expérience utilisateur des composants clés (Homepage Hero, Fiche Produit PDP, Catalogue PLP, Panier Drawer AJAX).

---

## User Review Required

> [!IMPORTANT]
> **Validation du Style Visuel :**
> Nous allons générer et concevoir les déclinaisons graphiques du logo TORNADO (Typographie bold géométrique + Vortex abstrait) et la palette de couleurs dorées/sombres.
> Merci d'indiquer si vous souhaitez des ajustements particuliers sur les nuances (ex. Or métallisé brillant vs Or mat champagne).

---

## Proposed Changes

### [Branding & Visual Identity]

#### [NEW] [logo-tornado-combined.svg](file:///home/hahi17/.gemini/antigravity/brain/6381d2f9-3bc9-4a2e-8a8d-170cb29e48fe/assets/logo-tornado-combined.svg)
Logo complet avec Wordmark TORNADO + Symbole Vortex.

#### [NEW] [logo-vortex-symbol.svg](file:///home/hahi17/.gemini/antigravity/brain/6381d2f9-3bc9-4a2e-8a8d-170cb29e48fe/assets/logo-vortex-symbol.svg)
Symbole Vortex autonome pour Favicon et responsive mobile.

---

### [Design System CSS]

#### [NEW] [tornado-tokens.css](file:///home/hahi17/.gemini/antigravity/brain/6381d2f9-3bc9-4a2e-8a8d-170cb29e48fe/assets/tornado-tokens.css)
Fichier CSS réutilisable définissant les tokens de design (Couleurs, Typographies, Radii, Animations, Z-index, Media queries).

---

### [UI Mockups & Concept Visuals]

#### [NEW] [design_system_spec.md](file:///home/hahi17/.gemini/antigravity/brain/6381d2f9-3bc9-4a2e-8a8d-170cb29e48fe/design_system_spec.md)
Documentation complète du Design System TORNADO avec guides d'utilisation des composants et aperçus visuels.

---

## Verification Plan

### Automated Tests
- Validation de la syntaxe CSS via linter.
- Vérification de la conformité SVG et du rendu vectoriel à toutes les résolutions.

### Manual Verification
- Contrôle des ratios de contraste WCAG 2.1 AA (Texte blanc & accent or sur fond noir obsidian).
- Vérification du rendu favicon et des icônes sur mobile et desktop.
