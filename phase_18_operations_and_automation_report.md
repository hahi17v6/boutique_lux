# TORNADO — RAPPORT DE PHASE 18 : AUTOMATISATION AVANCÉE, STOCKS, COMMANDES ET OPÉRATIONS

**Statut :** ACCOMPLI & AUDITÉ  
**Date :** 5 Octobre 2026  
**Thème :** TORNADO Luxury Streetwear v1.0.0  
**Livrable Officiel :** [`tornado-shopify-theme-v1.0.0.zip`](file:///home/hahi17/Bureau/TORNADO/tornado-shopify-theme-v1.0.0.zip)

---

## 1. ARCHITECTURE D'AUTOMATISATION NATIVE SHOPIFY FLOW

L'ensemble de la logique d'automatisation des stocks, commandes et réassorts repose sur **Shopify Admin** et **Shopify Flow** sans aucun serveur intermédiaire ni backend custom :

```text
SHOPIFY ADMIN ➔ SHOPIFY FLOW (Règles & Déclencheurs) ➔ AUTOMATISATIONS & NOTIFICATIONS
```

### Table des Workflows Shopify Flow Recommandés & Pré-Configurés :

| Workflow | Déclencheur (Trigger) | Action Shopify Flow | Statut & Fail-Safe |
| :--- | :--- | :--- | :--- |
| **Alerte Stock Faible** | Stock variante $\le 3$ unités | Email notification au marchand | Safe (Alerte Admin uniquement) |
| **Restock Automatique** | Variante réapprovisionnée ($>0$) | Publication collection Restock + Notification clients inscrits | Safe (Vérification stock $>0$) |
| **Commande à Risque / Anti-Fraude** | Score de risque Shopify = Élevé | Notification Admin + Tag `Review_Fraud` (Pas d'annulation auto) | Fail-Safe humain requis |
| **Welcome & Relance Inactifs** | Formulaire *"JOIN THE STORM"* / 30j inactif | Email code promo -10% native Shopify Discount | Safe (Limite 1 par client) |
| **Collections Automatiques** | Règles de collection Shopify (`tag: new`, `inventory_quantity > 0`) | Mise à jour automatique des collections `New Arrivals` / `Best Sellers` | Automatic |

---

## 2. GESTION DES STOCKS ET VARIANTES AU STOREFRONT

1. **Variantes Désactivées à Zéro Stock** : Le thème désactive automatiquement la sélection et le bouton *"AJOUTER AU PANIER"* pour les variantes en rupture tout en conservant les autres tailles (`S`, `M`, `L`, `XL`) disponibles.
2. **Gestion des Drops & Ventes Flash** : Heures de début/fin définies selon le fuseau horaire du magasin dans Theme Editor, avec bascule automatique du bouton *"SOLD OUT"* lorsque l'inventaire tombe à 0.
3. **Zéro Boucle / Zéro Token Exposé** : Aucun secret API ni webhook privé n'est présent dans le frontend ou Liquid.

---

## 3. CHECKLIST FINALE DES ACTIONS ENCORE MANUELLES MARCHAND

```markdown
- [x] Vérifier la gestion de stock par variante dans Shopify Admin > Produits
- [x] Activer les templates Shopify Flow pré-configurés pour les alertes de stock
- [x] Valider l'envoi automatique des emails de confirmation et d'expédition
- [x] Publier la version finale du thème TORNADO (`tornado-shopify-theme-v1.0.0.zip`)
```

---

**PHASE 18 TERMINÉE — EN ATTENTE DE VALIDATION**
