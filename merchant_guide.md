# TORNADO — MANUEL D'EXPLOITATION MARCHAND (SHOPIFY ADMIN)

Ce manuel rassemble toutes les procédures opérationnelles pour gérer quotidiennement la boutique **TORNADO** directement depuis **Shopify Admin**, sans jamais toucher au code.

---

## 1. GESTION DES PRODUITS & VARIANTES

### Ajouter un nouveau produit
1. Allez dans **Shopify Admin > Produits > Ajouter un produit**.
2. Renseignez :
   - **Titre** : ex: *HOODIE OBSIDIAN VORTEX*
   - **Description** : Description détaillée et histoire de la pièce.
   - **Médias** : Ajoutez au minimum 3 photos haute définition (fond sombre/neutre) et éventuellement une vidéo courte.
   - **Prix** : Prix de vente principal (ex: `180.00 €`).
   - **Prix comparatif** : (Optionnel) Pour afficher une réduction ou un prix barré d'archive (ex: `220.00 €`).
   - **Variantes** : Activez l'option pour les Tailles (*S, M, L, XL*) et Couleurs (*Noir Obscur, Or Champagne*).
   - **Stock** : Renseignez la quantité réelle disponible par variante.

---

## 2. CONFIGURATION DES METAFIELDS

Les metafields permettent d'enrichir automatiquement les fiches produits sans modifier le thème.

Allez dans **Shopify Admin > Paramètres > Données personnalisées > Produits** et créez les champs suivants :

| Nom du Metafield | Clé d'Espace de Noms (`Namespace.key`) | Type | Usage |
|---|---|---|---|
| **Composition Textile** | `custom.material_composition` | Texte sur une seule ligne | Ex: *100% Coton Lourd 450 gsm* |
| **Entretien Textile** | `custom.care_instructions` | Texte multi-lignes | Ex: *Lavage en machine à 30°C sur envers...* |
| **Guide des Tailles** | `custom.size_guide` | Texte enrichi (Richtext) | Tableau des mensurations sur-mesure |
| **Nom du Drop** | `custom.drop_name` | Texte sur une seule ligne | Ex: *DROP #04 — VORTEX* |

---

## 3. GESTION DES DROPS ("THE STORM DROPS")

Pour créer ou modifier un Drop exclusif :
1. Allez dans **Shopify Admin > Pages > Ajouter une page** (ou modifiez la page Drop existante).
2. Attribuez le modèle de page : `page.drop`.
3. Cliquez sur **Personnaliser le Thème** (Theme Editor) sur cette page :
   - **Statut du Drop** : Sélectionnez `UPCOMING` (À venir), `LIVE` (En ligne), ou `ENDED` (Terminé).
   - **Date de lancement ISO** : Renseignez la date exacte (ex: `2026-11-15T20:00:00`). Le compte à rebours se calculera automatiquement en secondes.
   - **Collection du Drop** : Sélectionnez la collection d'articles associés au Drop.

---

## 4. PROMOTIONS & CODE PROMO -10% ("STORM10")

Pour activer le code promo de bienvenue de la newsletter :
1. Allez dans **Shopify Admin > Réductions > Créer une réduction**.
2. Sélectionnez **Code de réduction**.
3. Renseignez :
   - **Code** : `STORM10`
   - **Valeur** : Pourcentage -> `10 %`
   - **Conditions d'éligibilité** : *Première commande par client*.
4. Sauvegardez. Le pop-up et la section newsletter distribuera ce code valide.

---

## 5. AUTOMATISATIONS SHOPIFY FLOW

Pour automatiser la gestion des stocks et de la sécurité :
- **Alerte Stock Faible** : Créez une règle Shopify Flow déclenchée sur *Inventory quantity changed* &rarr; Si stock <= 5 &rarr; Envoyer un email de réapprovisionnement à l'équipe TORNADO.
- **Tagging Client VIP** : Si le montant total des commandes d'un client >= 500 € &rarr; Ajouter le tag `VIP_CERCLE_TORNADO`.

---

## 6. EXPÉDITIONS & TRANSPORTEURS

1. Allez dans **Shopify Admin > Expédition et livraison**.
2. Configurez les tarifs :
   - **France & Europe** : Livraison Standard (`4,90 €`), Gratuite dès `150,00 €`.
   - **Express 24-48h** : `9,90 €`.
3. Lors du traitement d'une commande (*Fulfillment*), saisissez le numéro de suivi du transporteur (Chronopost, Colissimo, DHL). Le client recevra automatiquement la notification avec le lien officiel de suivi.
