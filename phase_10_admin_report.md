# TORNADO — RAPPORT DE PHASE 10 : ADMIN SHOPIFY & GESTION OPÉRATIONNELLE

**Statut :** ACCOMPLI (100% Autonome sans modification de code)  
**Date :** 5 Octobre 2026  
**Thème :** TORNADO Luxury Streetwear v1.0.0  

---

## 1. ARCHITECTURE D'EXPLOITATION MARCHAND

La **Phase 10** garantit que le propriétaire de la boutique **TORNADO** peut piloter 100% de son catalogue, de ses drops et de ses campagnes depuis **Shopify Admin** sans jamais ouvrir de fichier de code.

---

## 2. ÉLÉMENTS ADMINISTRABLES SANS CODE

### A. Metafields Produits Standardisés
- `custom.material_composition` : Composition des tissus (ex: *100% Coton Lourd 450 gsm*).
- `custom.care_instructions` : Recommandations d'entretien textile.
- `custom.size_guide` : Guide des tailles sur-mesure.
- `custom.drop_name` : Nom du Drop rattaché.

### B. Gestion des Drops ("THE STORM DROPS")
- **Statuts dynamiques** : Passage à l'état `UPCOMING`, `LIVE`, ou `ENDED` depuis l'éditeur de page `page.drop`.
- **Date de lancement ISO** : Décompte temporisé en secondes calculé automatiquement d'après l'horloge système Shopify.

### C. Theme Editor OS 2.0
- Paramétrage visuel complet des bannières, de la barre d'annonce top, du seuil de livraison offerte (150 €), des Ventes Flash et du pop-up de capture newsletter.

---

## 3. DOCUMENTATION LIVRÉE

- Manuel d'Exploitation Marchand : [`merchant_guide.md`](file:///home/hahi17/Bureau/TORNADO/merchant_guide.md).

---

**PHASE 10 TERMINÉE — EN ATTENTE DE VALIDATION**
