# TORNADO — RAPPORT DU CATALOGUE, RECHERCHE & FILTRES (PHASE 4)

---

## 1. FICHIERS CRÉÉS ET MODIFIÉS

* **Sections Liquid Shopify OS 2.0 :**
  * `sections/main-collection.liquid` (Page Liste de Produits PLP avec barre d'outils, filtres sidebar/drawer et états vides)
  * `sections/main-search.liquid` (Page de recherche complète avec formulaire, suggestions populaires et grille de résultats)
* **Assets CSS & JS :**
  * `assets/tornado-theme.css` (Styles du layout PLP, toolbar, chips de taille, tiroir de filtres mobile et modal de recherche)
  * `assets/tornado-theme.js` (Gestionnaire JS du tiroir de filtres mobile, tri dynamique et Predictive Search API `/search/suggest.json`)
* **Archive ZIP Mise à Jour :**
  * 📦 [`tornado-shopify-theme.zip`](file:///home/hahi17/Bureau/TORNADO/tornado-shopify-theme.zip)

---

## 2. COLLECTIONS CONFIGURÉES DANS L'ARCHITECTURE

* `Tous les produits` (`/collections/all`)
* `Sweats & Hoodies` (`/collections/sweats`)
* `Vestes` (`/collections/vestes`)
* `Pantalons & Cargos` (`/collections/pantalons`)
* `Sneakers` (`/collections/sneakers`)
* `Casquettes & Bonnets` (`/collections/casquettes`)
* `Sacs & Maroquinerie` (`/collections/sacs`)
* `Bijoux & Accessoires` (`/collections/bijoux` et `/collections/accessoires`)
* `Nouveautés` (`/collections/new-drops`)
* `Best-Sellers` (`/collections/best-sellers`)
* `Promotions & Archives` (`/collections/promotions`)

---

## 3. FILTRES CRÉÉS (DESKTOP & MOBILE DRAWER)

* **Par Marque :** TORNADO LABS, VALENTINO STUDIO, OBSIDIAN PARIS, ATELIER GOLD.
* **Par Taille :** Chips de taille interactives (`XS`, `S`, `M`, `L`, `XL`, `XXL`).
* **Par Disponibilité :** Filtre "En Stock uniquement".
* **Par Prix & Promotions :** Intégration native des facettes d'intervalle de prix Shopify.
* **Tiroir Mobile (`.filter-drawer`) :** Ouverture tactile dédiée via le bouton `FILTRES ET TRI`.

---

## 4. DONNÉES ET METAFIELDS NÉCESSAIRES SUR SHOPIFY

* **Tags Produits :** `NEW`, `Drop`, `LIMITED`, `BestSeller` pour le déclenchement automatique des badges.
* **Options de Variantes :** `Size` / `Taille` pour l'affichage dynamique des chips.
* **Metafields Recommandés :** `custom.fit_type` (Coupe Oversize / Taille normalement) et `custom.care_instructions`.

---

## 5. FONCTIONNALITÉS TERMINÉES

* Moteur de recherche prédictive réactif avec requêtes en temps réel `/search/suggest.json`.
* Conservation de l'état des filtres dans l'URL.
* Maintien du ratio d'aspect 3:4 uniforme sur toutes les cartes produits.
* Gestion élégante des états d'erreur et de recherche vide (`NOTHING HERE YET.`).

---

## 6. FONCTIONNALITÉS DEPENDANTES DE LA CONFIGURATION SHOPIFY

* L'activation de la Predictive Search avancée nécessite que l'application gratuite **Shopify Search & Discovery** soit installée sur la boutique Shopify pour configurer les synonymes et filtres personnalisés.

---

## 7. BUGS TROUVÉS ET CORRIGÉS

1. **Débordement du tiroir de filtres sur mobile :** Ajout de `overflow-y: auto` sur le corps du drawer.
2. **Double déclenchement de la recherche prédicitive :** Implémentation d'un délai de debounce de 250ms sur l'événement `input`.

---

## 8. PROCÉDURE DE TEST DANS SHOPIFY

1. Importer l'archive mise à jour : [`tornado-shopify-theme.zip`](file:///home/hahi17/Bureau/TORNADO/tornado-shopify-theme.zip) dans Shopify Admin.
2. Naviguer vers une collection (ex: `/collections/all`).
3. Tester les filtres par taille et le tri.
4. Ouvrir la modal de recherche et saisir "Hoodie" pour tester la Predictive Search.

---

**PHASE 4 TERMINÉE — EN ATTENTE DE VALIDATION**
