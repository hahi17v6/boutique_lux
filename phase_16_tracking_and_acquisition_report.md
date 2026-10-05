# TORNADO — RAPPORT DE PHASE 16 : ACQUISITION, PUBLICITÉ ET TRACKING E-COMMERCE

**Statut :** ACCOMPLI & AUDITÉ  
**Date :** 5 Octobre 2026  
**Thème :** TORNADO Luxury Streetwear v1.0.0  
**Livrable Officiel :** [`tornado-shopify-theme-v1.0.0.zip`](file:///home/hahi17/Bureau/TORNADO/tornado-shopify-theme-v1.0.0.zip)

---

## 1. STRATÉGIE ET PROPRETÉ DU TRACKING E-COMMERCE

L'audit complet du code storefront TORNADO garantit un suivi publicitaire fiable sans dégrader la vitesse d'affichage ou violer les règles RGPD :

1. **Aucun Script Publicitaire Hardcodé dans le Code** :
   - Évite les conflits, le double comptage d'achats et le ralentissement du chargement (LCP).
   - Utilisation recommandée de **Shopify Customer Events / Customer Privacy API** dans **Shopify Admin > Paramètres > Événements client**.
2. **Open Graph & Rich Social Cards (Balises Méta)** :
   - Intégration dans `snippets/meta-tags.liquid` des métadonnées dynamiques e-commerce :
     - `og:price:amount` : Prix du produit (ex. `180.00`).
     - `og:price:currency` : Devise ISO (`EUR`).
     - `og:availability` : État des stocks (`instock` / `outofstock`).
     - `og:image` & `twitter:card` : Visuels grand format optimisés pour partages TikTok/Instagram.

---

## 2. CANAUX ET CONFIGURATION DES PIXELS (SHOPIFY PIXELS NATIFS)

| Canal / Plateforme | Mécanisme d'Intégration Recommandé | Événements Couverts |
| :--- | :--- | :--- |
| **Meta (Instagram / FB)** | App Officielle *Facebook & Instagram* sur Shopify | `PageView`, `ViewContent`, `AddToCart`, `InitiateCheckout`, `Purchase` |
| **TikTok Ads** | App Officielle *TikTok for Shopify* | `ViewContent`, `AddToCart`, `InitiateCheckout`, `Purchase` |
| **Google Analytics 4 & Ads** | App Officielle *Google & YouTube* / Merchant Center | `view_item`, `add_to_cart`, `begin_checkout`, `purchase` |

---

## 3. DESTRUCTURATION UTM & PARCOURS LANDING PAGES

TORNADO supporte les paramètres de campagne UTM pour l'attribution des ventes sans altérer l'expérience d'achat :

```text
https://tornado-brand.com/collections/drops?utm_source=tiktok&utm_medium=paid_social&utm_campaign=drop_vortex_01
```

- **TikTok / Instagram Organic** ➔ `/collections/drops` ou `/products/{handle}`
- **Google Shopping Ads** ➔ Fiches produits dédiées avec prix et devises pré-convertis
- **Influenceurs / Partenariats** ➔ Landing pages thématiques `/pages/{campaign-slug}`

---

## 4. CONFORMITÉ RGPD & DÉDUPLICATION DES ÉVÉNEMENTS

- **Consentement Préalable** : Intégration compatible avec la bannière de consentement native Shopify (`window.Shopify.customerPrivacy`).
- **Déduplication des Achats (`Purchase`)** : Gérée côté serveur par l'API Shopify pour éviter le double comptage lors des rafraîchissements de la page de confirmation (`thank_you`).

---

**PHASE 16 TERMINÉE — EN ATTENTE DE VALIDATION**
