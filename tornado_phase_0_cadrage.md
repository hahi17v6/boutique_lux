# TORNADO — PHASE 0 : DOSSIER DE CADRAGE COMPLET ET SPÉCIFICATIONS TECHNIQUES

---

## TABLE DES MATIÈRES
1. [Résumé du concept Tornado](#1-résumé-du-concept-tornado)
2. [Positionnement Marque & Marché](#2-positionnement-marque--marché)
3. [Cible & Profils Acheteurs](#3-cible--profils-acheteurs)
4. [Architecture Commerciale](#4-architecture-commerciale)
5. [Architecture Catalogue & Modèle de Données](#5-architecture-catalogue--modèle-de-données)
6. [Architecture de Navigation](#6-architecture-de-navigation)
7. [Structure & Wireframing des Pages Clefs](#7-structure--wireframing-des-pages-clefs)
8. [Matrice des Fonctionnalités](#8-matrice-des-fonctionnalités)
9. [Direction Artistique & Identité Visuelle](#9-direction-artistique--identité-visuelle)
10. [Design System & Charte Graphique](#10-design-system--charte-graphique)
11. [Expérience Utilisateur Mobile (Mobile-First)](#11-expérience-utilisateur-mobile-mobile-first)
12. [Expérience Utilisateur Desktop](#12-expérience-utilisateur-desktop)
13. [Stratégie de Drops & Événementialisation](#13-stratégie-de-drops--événementialisation)
14. [Stratégie Marketing & Acquisition](#14-stratégie-marketing--acquisition)
15. [Architecture Shopify Core & Stack Technique](#15-architecture-shopify-core--stack-technique)
16. [Politique de Sécurité & Conformité](#16-politique-de-sécurité--conformité)
17. [Stratégie de Performance Web & Vitesse](#17-stratégie-de-performance-web--vitesse)
18. [Stratégie SEO (Référencement Naturel)](#18-stratégie-seo-référencement-naturel)
19. [Accessibilité Web (WCAG 2.1 AA)](#19-accessibilité-web-wcag-21-aa)
20. [Analyse des Risques Techniques](#20-analyse-des-risques-techniques)
21. [Analyse des Risques Business & Juridiques](#21-analyse-des-risques-business--juridiques)
22. [Synthèse des Points à Valider par le Fondateur](#22-synthèse-des-points-à-valider-par-le-fondateur)
23. [Roadmap Détaillée des Phases Suivantes (Phases 1 à 6)](#23-roadmap-détaillée-des-phases-suivantes-phases-1-à-6)

---

## 1. RÉSUMÉ DU CONCEPT TORNADO

**TORNADO** est une marque et plateforme e-commerce haut de gamme positionnée à l'intersection du **luxe contemporain** et du **streetwear haut de gamme**.

La vision de TORNADO repose sur trois piliers fondamentaux :
1. **L'Attraction Visuelle Immédiate (The Wow Effect) :** Une expérience digitale immersive, éditoriale et extravagante, tranchant radicalement avec l'esthétique générique et répétitive des boutiques dropshipping traditionnelles.
2. **Le Désir & la Rareté (Hype Architecture) :** Une scénarisation des collections sous forme de "drops", d'éditions limitées et de ventes événementielles pour stimuler l'achat d'impulsion et la fidélisation.
3. **Une Performance Marchande Sans Friction :** Une boutique ultra-rapide sur mobile, exploitant la robustesse du cœur marchand de Shopify (panier AJAX, checkout en 1 clic Stripe/Apple Pay, sécurité native).

---

## 2. POSITIONNEMENT MARQUE & MARCHÉ

* **Créneau :** Luxury Streetwear Accessible / Premium Streetwear.
* **Gamme de Prix :** Majoritairement **100 € à 250 €** au lancement. Pas d'articles d'entrée de gamme low-cost (< 40 €) ni d'articles de haute couture inaccessible (> 500 €).
* **Proposition de Valeur :** Offrir le prestige visuel et l'exclusivité d'une maison de luxe (type Balenciaga, Off-White, Fear of God) avec une accessibilité tarifaire maîtrisée et une sélection streetwear pointue.
* **Différenciation :**
  * Zéro sensation de "dropshipping basique" (typographies soignées, compositions bento/grid éditoriales, narration forte).
  * Palette sombre et dorée sophistiquée (noir profond, blanc pur, accents or métallisé).
  * Transparence logistique et valorisation produit par des visuels haute définition.

---

## 3. CIBLE & PROFILS ACHETEURS

* **Tranche d'âge principale :** **14 à 40 ans**.
  * *Cœur de cible (18–30 ans) :* Passionnés de streetwear, d'exclusivité, sensibles à la culture drop, utilisateurs TikTok/Instagram.
  * *Cible secondaire (31–40 ans) :* Amateurs de mode urbaine haut de gamme recherchant des pièces fortes et bien coupées avec un pouvoir d'achat plus élevé.
  * *Cible jeune (14–17 ans) :* Prescripteurs de tendances influencés par les réseaux sociaux (achat financé ou auto-financé).
* **Zone Géographique :**
  * **Phase A :** Lancement France.
  * **Phase B :** Expansion Union Européenne, Royaume-Uni, Suisse.
* **Comportement d'achat :** Achat d'impulsion sur mobile (80%+ du trafic), exigeant une rapidité d'affichage sous les 2 secondes et des méthodes de paiement instantanées (Apple Pay, Google Pay).

---

## 4. ARCHITECTURE COMMERCIALE

* **Plateforme Cœur :** Shopify (Plan Basic ou Shopify Standard selon volume initial).
* **Panier Moyen Cible (AOV) :** **130 € – 180 €**.
* **Politique de Livraison :**
  * **Livraison offerte :** À partir de **150 € d'achat** (mécanisme d'upsell incitant à ajouter un accessoire ou un T-shirt).
  * **Frais de livraison sous 150 € :** Tarification fixe zone France (ex. 4,90 € à 6,90 € standard) **À VALIDER**.
* **Moyens de Paiement Intégrés :**
  * Stripe / Shopify Payments (Cartes Visa, Mastercard, AMEX).
  * Apple Pay & Google Pay (Paiement 1-tap mobile).
  * Paiement en 3x/4x sans frais via Klarna ou Alma (**À VALIDER** pour booster la conversion sur les paniers > 150 €).

---

## 5. ARCHITECTURE CATALOGUE & MODÈLE DE DONNÉES

### 5.1 Volume & Catégorisation au Lancement (~100 SKUs)
1. **Sweats** (Hoodies, Crewnecks oversize)
2. **Vestes** (Puffers, Jackets techniques, Teddy)
3. **Pantalons** (Cargo premium, Joggers structurés, Denims)
4. **Sneakers** (Running futuristes, Low-top luxury)
5. **Casquettes** (Caps structurées, Beanies)
6. **Sacs** (Crossbody bags, Backpacks, Chest rig)
7. **Bijoux** (Chaînes acier/argent/or, Bagues, Bracelets)
8. **T-shirts** (Heavyweight cotton, Oversized graphic tees)
9. **Accessoires** (Ceintures, Portefeuilles, Chaussettes)
10. **Nouveautés** (Filtre dynamique / Collection automatisée)
11. **Best-sellers** (Filtre dynamique / Collection automatisée)

### 5.2 Schéma des Métadonnées Produit (Standard Shopify Extended)
Chaque fiche produit comporte impérativement :
* `ID / Handle` (slug URL optimisé SEO)
* `Title` (ex: *TORNADO Oversized Puffer Jacket — Champagne Gold*)
* `Vendor / Brand` (Marque propre TORNADO ou Marque partenaire vérifiée)
* `Product Type` (Catégorie parent)
* `Description` (Rédactionnelle luxe + Guide des tailles + Composition/Entretien)
* `Price` & `Compare At Price` (Gestion des promotions/ancien prix)
* `SKU & Barcode / EAN`
* `Variants` : Taille (XS, S, M, L, XL, XXL) x Couleur (Black, White, Gold, Gray)
* `Inventory Quantity` (Stock réel synchronisé)
* `Tags` (`Drop_2026_01`, `BestSeller`, `Limited_500`, `Material_Cotton400gsm`)
* `Metafields Personnalisés` :
  * `custom.care_instructions` (Instructions de lavage)
  * `custom.fit_type` (Taille normalement / Coupe Oversize)
  * `custom.model_height_size` (Taille du mannequin & taille portée)
  * `custom.launch_date` (Horodatage de lancement pour compte à rebours drop)
  * `custom.badge_status` (`NEW DROP`, `LIMITED`, `SALE`, `SOON`)

### 5.3 Politique Rigoille sur les Marques Tiers (Marques Luxury)
> [!CAUTION]
> **RÈGLE JURIDIQUE STRICTE SUR LES MARQUES DE LUXE (Dior, Moncler, Burberry, etc.) :**
> Aucune marque déposée ne sera affichée sur la boutique sans la possession physique des preuves d'authenticité, des factures d'approvisionnement licites au sein du marché de l'UE (principe d'épuisement des droits) et la vérification préalable des droits de revente. Tout produit suspect ou non documenté sera banni du catalogue pour prévenir tout risque de contrefaçon, fermeture de compte Shopify ou poursuite judiciaire.

---

## 6. ARCHITECTURE DE NAVIGATION

```
[ HEADER GLOBAL ]
├── Logo TORNADO + Vortex (Gauche / Centre sur Mobile)
├── Menu Principal (Desktop Center)
│   ├── SHOP ▾
│   │   ├── Tous les produits
│   │   ├── Sweats & Hoodies
│   │   ├── Vestes & Manteaux
│   │   ├── Pantalons & Cargos
│   │   ├── Sneakers
│   │   ├── Casquettes & Bonnets
│   │   ├── Sacs & Maroquinerie
│   │   ├── Bijoux
│   │   └── Accessoires
│   ├── DISCOVER ▾
│   │   ├── Nouveautés (New Drops)
│   │   ├── Best-Sellers
│   │   ├── Éditions Limitées
│   │   └── Ventes Flash / Archive
│   └── BRANDS (Marques sélectionnées)
├── Barre de Recherche Instantanée (Predictive Search)
├── Icône Wishlist (avec compteur dynamique)
├── Icône Compte (Optionnel / Discret)
└── Icône Panier Drawer (avec compteur & badge d'offres)
```

---

## 7. STRUCTURE & WIREFRAMING DES PAGES CLEFS

### 7.1 Homepage (Page d'Accueil)
* **Hero Banner Immersif :** Vidéo de marque haute définition en boucle (loop silencieux MP4/WebM) ou carrousel visuel full-bleed avec superposition de typographie géante et CTA doré (*"DISCOVER THE DROP"*).
* **Ticker de Marque Animé (Marquee text) :** Bandeau défilant fluide (*"FREE SHIPPING OVER 150€ — LIMITED QUANTITIES — WORLDWIDE EXPRESS"*).
* **Grid Bento "Featured Categories" :** Pavés asymétriques mettant en valeur les catégories phares (Sweats, Sneakers, Sacs).
* **Section Drop en Cours / Compte à Rebours :** Bloc sombre avec compte à rebours dynamique pour le prochain release et aperçu flouté/preview des pièces.
* **Carrousel "Nouveautés & Best-Sellers" :** Grille produit 4 colonnes (desktop) / 2 colonnes (mobile) avec boutons de rapide *"Ajout au panier"* et hover image secondaires.
* **Section Narration / Brand Manifesto :** Bloc éditorial en typographie bold contrastée (*"LUXURY MEETS THE STREET"*).
* **Section "Join The Storm" (Newsletter VIP) :** Formulaire de capture email épuré avec incitation (-10% sur la 1ère commande **À VALIDER**).
* **Footer Complet :** Reassurance (Paiement Stripe sécurisé, Livraison rapide, Service Client), liens légaux, devises, réseaux sociaux.

### 7.2 Page Liste Produits / Collections (PLP)
* **Header de Collection :** Titre en grand format, court texte éditorial, image de couverture optionnelle.
* **Barre d'Outils Filtres Sticky :**
  * Filtre par Marque, Catégorie, Taille (XS à XXL), Couleur, Tranche de Prix, Disponibilité (En Stock / Sur Commande).
  * Tri : Pertinence, Nouveautés, Prix croissant/décroissant, Meilleures ventes.
  * Switcheur de vue grille (2 colonnes vs 4 colonnes).
* **Cartes Produits :** Image principale + Image au survol (hover effect), badge d'exclusivité, titre, marque, prix barré/prix actuel, sélecteur rapide de taille au survol.

### 7.3 Fiche Produit (PDP - Product Detail Page)
* **Galerie Visuelle :**
  * *Desktop :* Grille 2x2 d'images haute résolution avec zoom au survol.
  * *Mobile :* Swiper/Carrousel horizontal avec indicateur de pagination à points et pincement pour zoomer.
* **Panneau d'Achat (Sticky à droite sur Desktop) :**
  * Fil d'Ariane (Home > Sweats > Hoodie Black Tornado)
  * Titre Produit & Marque
  * Prix (avec affichage clair des taxes et de l'économie réalisée si promotion)
  * Sélecteur de Taille interactif (avec indicateur de stock faible sur les tailles critiques, ex: *"Plus que 2 en stock"*).
  * Bouton "Guide des Tailles" déclenchant une modale sur-mesure.
  * CTA Principal : *"AJOUTER AU PANIER"* (Bouton d'accentuation haute visibilité avec effet au survol).
  * CTA Secondaire : *"BUY WITH APPLE PAY / STRIPE"* (Bouton dynamique Shopify).
  * Bouton d'ajout à la Wishlist (icône cœur).
* **Blocs Accordéons Droulants (Collapsible Tabs) :**
  * Description & Coupe produit
  * Matières, Composition & Entretien
  * Délais de Livraison & Politique de Retour
* **Section "Complete The Look" (Cross-sell) :** Suggestion d'articles assortis (ex: Pantalon + Casquette assortis).
* **Section Avis Clients Authentiques :** Étoiles, commentaires filtrables, métriques de taille (ex: *"Taille correctement"*).
* **Produits Vus Récemment / Recommandations IA.**

### 7.4 Panier Drawer (Side-Cart AJAX)
* Glissement fluide depuis la droite sans rechargement de page.
* Jauge de progression visuelle : *"Plus que XX € pour bénéficier de la LIVRAISON GRATUITE !"*.
* Liste des articles avec miniature, variante, sélecteur de quantité rapide (+/-) et suppression.
* Zone de code promo/réduction intégrée.
* Sous-total clair et bouton explicite *"PASSER À LA CAISSE"* redirigeant vers le checkout Stripe sécurisé de Shopify.

---

## 8. MATRICE DES FONCTIONNALITÉS

| Fonctionnalité | Description Technique | Implémentation | Statut |
| :--- | :--- | :--- | :--- |
| **Guest Checkout** | Achat fluide sans création de compte obligatoire | Natif Shopify Core | Validé |
| **Paiement Stripe / CB** | Traitement sécurisé des cartes banquaires | Shopify Payments / Stripe | Validé |
| **Paiement Mobile 1-Tap** | Apple Pay / Google Pay intégrés au panier | Natif Shopify | Validé |
| **Panier Drawer AJAX** | Panier latéral coulissant sans rechargement | Custom Liquid / JS Vanilla | Validé |
| **Jauge Livraison Gratuite** | Calcule le montant restant pour atteindre 150 € | JS Vanilla dans Cart Drawer | Validé |
| **Wishlist Sans Compte** | Sauvegarde des favoris dans le localStorage du navigateur | Custom JS + Synchro Compte | Validé |
| **Filtres Avancés** | Filtrage multi-critères instantané | Search & Discovery API Shopify | Validé |
| **Compte à Rebours Drop** | Timer dynamique pour les lancements | Custom Section Liquid | Validé |
| **Système d'Avis** | Notes, commentaires, filtres et modération | App Native Légère / Judge.me | Validé |
| **Newsletter "Join The Storm"**| Inscription email + coupon automatique | Klaviyo / Shopify Email | Validé |
| **Guide des Tailles Modale** | Tableau de mesures par catégorie | Modale CSS/JS native | Validé |
| **Paiement 3x / 4x** | Solution de paiement fractionné (Klarna/Alma) | Module Stripe/Klarna | **À VALIDER** |

---

## 9. DIRECTION ARTISTIQUE & IDENTITÉ VISUELLE

### 9.1 Concept Esthétique : "Dark Luxury & High Voltage Streetwear"
L'esthétique de TORNADO s'inspire des codes visuels de la haute couture contemporaine et des galeries d'art underground : contrastes violents, typographies massives, lignes épurées et touches d'or métallisé qui apportent un statut premium sans surcharger la lisibilité.

### 9.2 Palette de Couleurs (Tokens Design)

```css
:root {
  /* Couleurs Principales */
  --color-bg-primary: #0A0A0A;        /* Noir Profond Obsidian (Fond principal) */
  --color-bg-surface: #141414;        /* Noir Anthracite (Cartes & Modales) */
  --color-text-primary: #FFFFFF;      /* Blanc Pur (Titres & Textes d'impact) */
  --color-text-secondary: #A0A0A0;    /* Gris Neutre (Sous-titres & Métadonnées) */
  
  /* Accentuation Luxe */
  --color-accent-gold: #D4AF37;       /* Or Champagne Métallisé (Boutons, Badges, Highlights) */
  --color-accent-gold-hover: #E5C158; /* Or Lumineux (Hover States) */
  
  /* Éléments Système */
  --color-border: #262626;            /* Lignes de séparation discrètes */
  --color-error: #FF4D4D;             /* Rouge Alerte (Erreurs & Stock critique) */
  --color-success: #00E676;           /* Vert Validation */
}
```

---

## 10. DESIGN SYSTEM & CHARTE GRAPHIQUE

### 10.1 Typographie
* **Titres & Display (Headings & Hero) :** Typographie sans-serif géométrique, moderne et ultra-bold (ex. *Syne*, *Outfit*, ou *Monument Extended* via Google Fonts).
* **Corps de Texte & Interface (Body & UI) :** Typographie ultra-lisible, neutre et responsive (ex. *Inter* ou *Roboto*).

### 10.2 Logo & Symbole TORNADO
* **Wordmark :** Typographie custom "TORNADO" à empattements minimalistes et lettres espacées (tracking large).
* **Symbole (Vortex Tornado) :** Icône géométrique abstraite représentative d'une tornade stilysée.
* **Déclinaisons :**
  * Version combinée (Logo + Symbole) pour Header Desktop et Packaging.
  * Version Symbole Seul pour Favicon (32x32px), icône d'application mobile, bouton mobile et griffe textile.

---

## 11. EXPÉRIENCE UTILISATEUR MOBILE (MOBILE-FIRST)

Étant donné que **80% à 85% du trafic** sur le segment streetwear/mode provient du mobile :
* **Zones de Toucher Optimisées (Thumb-Zone) :** Boutons d'action principaux (Ajouter au panier, Checkout) positionnés en bas de l'écran, d'une hauteur minimale de **48px** pour éviter les faux clics.
* **Navigation à Tiroir (Hamburger Menu Premium) :** Ouverture fluide avec catégories claires, raccourcis vers les drops actuels et sélecteur de langue/devise.
* **Gestures Touch :** Carrousels d'images produit avec balayage naturel (swipe) et indicateur visuel.
* **Vitesse de Réponse :** Chargement asynchrone des composants interactifs pour zéro décalage au toucher.

---

## 12. EXPÉRIENCE UTILISATEUR DESKTOP

* **Mise en Page Éditoriale Grand Écran :** Exploitation des résolutions HD (1440px et 1920px) avec des grilles asymétriques (Bento grids) et des visuels grand format.
* **Effets au Survol (Hover Interactions) :** Prévisualisation instantanée de la seconde image produit, apparition des tailles disponibles au survol de la carte produit.
* **Raccourci Clavier de Recherche :** Appuyer sur `/` ou `Ctrl+K` ouvre instantanément la recherche produit globale.

---

## 13. STRATÉGIE DE DROPS & ÉVÉNEMENTIALISATION

1. **Teasing & Compte à Rebours :** Affichage d'une bannière dynamique sur le site 7 jours avant chaque drop.
2. **Access Anticipé VIP ("JOIN THE STORM") :** Les abonnés à la newsletter reçoivent un mot de passe ou un lien privé pour accéder au site 1 heure avant l'ouverture publique.
3. **Badges d'Urgence Authentiques :** Indicateurs visuels basés strictement sur l'état réel des stocks Shopify (`DERNIÈRES PIÈCES`, `STOCK ÉPUISÉ`, `ÉDITION LIMITÉE`). Aucune fausse urgence manipulatoire.

---

## 14. STRATÉGIE MARKETING & ACQUISITION

* **Canaux d'Acquisition Principaux :**
  * **TikTok & Instagram Reels :** Contenus vidéo courts axés sur le style, les matières, les unboxings et l'esthétique premium de TORNADO.
  * **Influence & Seeding :** Envoi de pièces clés à des créateurs de contenu mode/streetwear sélectionnés.
* **Retargeting & Emails Transactionnels :**
  * Séquence de bienvenue (Welcome Series) : Email 1 (-10% **À VALIDER**), Email 2 (Histoire de la marque), Email 3 (Découverte des Best-Sellers).
  * Relance de Panier Abandonné (3 relances automatiques à H+1, H+24 et H+48).

---

## 15. ARCHITECTURE SHOPIFY CORE & STACK TECHNIQUE

```
[ ARCHITECTURE TECHNIQUE TORNADO ]
┌──────────────────────────────────────────────────────────┐
│                    SHOPIFY CORE                          │
│  (Catalog, Variants, Orders, Checkout, Stripe, Customers)│
└────────────────────────────┬─────────────────────────────┘
                             │
       ┌─────────────────────┴─────────────────────┐
       ▼                                           ▼
┌────────────────────────────┐           ┌───────────────────┐
│ Custom Liquid OS 2.0 Theme │           │ Native API Layer  │
│ (HTML5 / Vanilla JS / CSS) │           │ (Storefront API,  │
└──────────────┬─────────────┘           │  Search&Discovery)│
               │                         └─────────┬─────────┘
               ▼                                   ▼
┌──────────────────────────────────────────────────────────┐
│              FRONTEND PREMIUM EXPERIENCE                 │
│ (Speed Optimized, No Heavy Apps, AJAX Cart, WebP Assets) │
└──────────────────────────────────────────────────────────┘
```

* **Philosophie "Zero-App Bloat" :** Limiter l'installation d'applications tierces payantes et lourdes. Utiliser les sections natives de Shopify Online Store 2.0 et du code JavaScript Vanilla optimisé pour garantir des temps de chargement records.

---

## 16. POLITIQUE DE SÉCURITÉ & CONFORMITÉ

* **Validation Côté Serveur Obligatoire :** Aucun prix ni montant de panier envoyé par le client n'est fait confiance. Tout le calcul est réexécuté au niveau de l'API Shopify et du module Stripe.
* **Webhooks Sécurisés :** Vérification des signatures HMAC SHA-256 sur l'ensemble des webhooks (Shopify / Stripe).
* **Protection XSS & Injection :** Échappement strict des données saisies par les utilisateurs dans les formulaires et les avis clients via les filtres de sécurité Liquid (`escape`, `json`).
* **Conformité RGPD :** Bannière de consentement aux cookies conforme, possibilité de suppression des données personnelles sur demande, aucune transmission de données non consenties.
* **Secrets et Clés API :** Aucune clé privée stockée dans le code frontend.

---

## 17. STRATÉGIE DE PERFORMANCE WEB & VITESSE

* **Objectifs Web Vitals :**
  * **Largest Contentful Paint (LCP) :** < 1,8s
  * **Interaction to Next Paint (INP) :** < 100ms
  * **Cumulative Layout Shift (CLS) :** < 0.05
  * **Score Google Lighthouse Mobile :** > 90/100
* **Techniques d'Optimisation :**
  * Format d'images modernes (WebP / AVIF) générés automatiquement par Shopify CDN.
  * Lazy loading natif (`loading="lazy"`) sur toutes les images sous la ligne de flottaison (offscreen).
  * Inlining des CSS critiques et chargement différé (`defer`) du JavaScript.
  * Pas de frameworks JS lourds (React/Vue non nécessaires pour le thème liquid nativement rapide).

---

## 18. STRATÉGIE SEO (RÉFÉRENCEMENT NATUREL)

* **Balisage Sémantique HTML5 :** Structure stricte (`header`, `nav`, `main`, `section`, `article`, `footer`).
* **Hierarchie des Titres :** Un seul `<h1>` unique par page, suivi d'une arborescence logique `<h2>` et `<h3>`.
* **Données Structurées JSON-LD :** Intégration des schémas Schema.org (`Product`, `Offer`, `AggregateRating`, `BreadcrumbList`, `Organization`).
* **URLs Propres :** URLs sans caractères spéciaux ni paramètres superflus (ex: `/collections/sweats/products/hoodie-black-tornado`).
* **Balisage Alt systématique :** Descriptions d'images optimisées pour l'accessibilité et le référencement d'images.

---

## 19. ACCESSIBILITÉ WEB (WCAG 2.1 AA)

* **Contraste des Couleurs :** Ratio de contraste supérieur à **4.5:1** pour l'ensemble des textes principaux (Texte Blanc sur Fond Noir Obsidian).
* **Navigation au Clavier :** Indicateurs de focus visuels clairs lors du déplacement avec la touche `Tab`.
* **Support des Lecteurs d'Écran :** Attributs ARIA (`aria-label`, `aria-expanded`, `aria-hidden`) correctement positionnés sur les boutons interactifs, modales et tiroir de panier.
* **Respect de `prefers-reduced-motion` :** Désactivation automatique des animations complexes pour les utilisateurs ayant activé l'option de réduction des mouvements.

---

## 20. ANALYSE DES RISQUES TECHNIQUES

| Risque Technique | Niveau d'Impact | Mesure de Mitigation Préventive |
| :--- | :--- | :--- |
| **Ruptures de stock Dropshipping** | Élevé | Synchronisation quotidienne des stocks via API fournisseur + alerte seuil bas |
| **Ralentissement par scripts tiers** | Moyen | Audit strict de chaque app ajoutée, chargement asynchrone des scripts analytics |
| **Bugs d'affichage Mobile Safari** | Moyen | Utilisation de `dvh` (Dynamic Viewport Height) au lieu de `100vh` pour éviter les décalages de barre d'adresse |
| **Surcharge lors d'un Drop (Pic de trafic)** | Élevé | Infrastructure Shopify Cloud nativement scalable pour absorber les pics sans crash |

---

## 21. ANALYSE DES RISQUES BUSINESS & JURIDIQUES

> [!WARNING]
> **ANALYSE DU RISQUE SUR LA POLITIQUE "SANS RETOUR" (DROIT DE RÉTRACTATION UE) :**
> **Risque Majeur :** En France et dans l'Union Européenne, la Directive 2011/83/UE accorde aux consommateurs un **droit de rétractation légal et obligatoire de 14 jours** pour tout achat effectué à distance (e-commerce), sans avoir à justifier de motif.
> **Conséquence :** Afficher une politique "Sans Retour" ou "Aucun remboursement" est **illégal** en Europe pour du prêt-à-porter standard. Cela expose la marque à des sanctions de la DGCCRF, des blocages Stripe/Shopify Payments et une perte de confiance des clients.
> **Recommandation :** Accepter les retours sous 14 jours aux frais du client, ou proposer des échanges / avoirs valables sur les drops futurs (**À VALIDER URGENT**).

---

## 22. SYNTHÈSE DES POINTS À VALIDER PAR LE FONDATEUR

Voici la liste exacte des arbitrages stratégiques et juridiques nécessaires avant le lancement du développement (Phase 1) :

| # | Point à Valider | Options Proposées | Impact / Statut |
| :--- | :--- | :--- | :--- |
| **V1** | **Politique de Retour Légale** | A) Retours autorisés sous 14 jours (Conforme UE)<br>B) Échange / Avoir uniquement | **CRITIQUE** (Juridique & Stripe) |
| **V2** | **Vérification des Marques Luxe** | A) Uniquement la marque propre TORNADO au lancement<br>B) Revente de marques tiers avec certificats | **CRITIQUE** (Droit des marques) |
| **V3** | **Frais de Port sous 150 €** | A) Fixe 4,90 € (France)<br>B) Fixe 6,90 € (France + Europe) | Stratégie Commerciale |
| **V4** | **Offre Bienvenue Newsletter** | A) -10% sur 1ère commande<br>B) Accès anticipé exclusif aux Drops sans réduction | Marge & Marketing |
| **V5** | **Paiement Fractionné (3x/4x)** | A) Activation de Klarna / Alma<br>B) Paiement comptant uniquement (Stripe) | Taux de Conversion |
| **V6** | **Base du Thème Shopify** | A) Développement Custom Sections sur base Dawn 2.0 (Gratuit & Ultra Rapide)<br>B) Achat d'un thème Premium (Impact / Prestige ~350$) | Choix Budget / Dev |

---

## 23. ROADMAP DÉTAILLÉE DES PHASES SUIVANTES

```
┌─────────────────────────────────────────────────────────────────┐
│                      ROADMAP PROJET TORNADO                     │
└─────────────────────────────────────────────────────────────────┘
 ├── PHASE 0 : CADRAGE, SPÉCIFICATIONS & ANTAGONISMES (En cours)
 ├── PHASE 1 : DIRECTION ARTISTIQUE, LOGO & DESIGN SYSTEM (Figma / Assets)
 ├── PHASE 2 : CONFIGURATION SHOPIFY CORE & STRUCTURATION CATALOGUE
 ├── PHASE 3 : DÉVELOPPEMENT FRONTAL DU THÈME & SECTIONS OS 2.0
 ├── PHASE 4 : INTÉGRATION DES FONCTIONNALITÉS, STRIPE & APPS SÉCURISÉES
 ├── PHASE 5 : RECETTE CRITIQUE, OPTIMISATION PERFORMANCE & AUDIT SEO
 └── PHASE 6 : LANCEMENT COMMERCIAL & STRATÉGIE DE DROP #1
```

* **Phase 1 — Identity & Design System :** Finalisation vectorielle du logo TORNADO + Vortex, création des mockups de la homepage et des fiches produits, export des assets optimisés.
* **Phase 2 — Shopify Architecture & Catalogue Setup :** Configuration des taxes, zones de livraison, catégories, métadonnées, insertion des 100 produits initiaux avec visuels calibrés.
* **Phase 3 — Theme Frontend Development :** Coder les sections Liquid 2.0 (Hero vidéo, Grilles Bento, PDP éditoriale, Panier Drawer AJAX).
* **Phase 4 — Integrations & Security :** Connexion Stripe, Apple Pay, Klaviyo/Shopify Email, Wishlist, Avis clients, tests d'étanchéité des formulaires.
* **Phase 5 — QA, Performance & SEO Audit :** Tests d'affichage cross-browser/mobile, validation des scores Lighthouse (>90), validation W3C et contrôles RGPD.
* **Phase 6 — Launch & Drop #1 Execution :** Lancement de la campagne de teasing, ouverture des accès VIP, suivi en direct des commandes et du panier moyen.

---

**PHASE 0 TERMINÉE — EN ATTENTE DE VALIDATION**
