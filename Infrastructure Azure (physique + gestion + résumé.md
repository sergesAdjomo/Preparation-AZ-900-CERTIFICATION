# 🏗️ Infrastructure Azure – Résumé de Module

---

## 🌍 1. Infrastructure physique

### 📌 Centres de données
- Base physique d’Azure (alimentation, refroidissement, réseau).  
- Regroupés en **régions** et **zones de disponibilité** (AZ).  
- Non accessibles directement aux clients.  

### 📌 Régions
- Zone géographique → ≥ 1 datacenter reliés par **réseau faible latence**.  
- Certaines ressources/services ne sont disponibles que dans certaines régions.  
- Services **globaux** (Entra ID, Traffic Manager, Azure DNS) → pas de choix de région.  

### 📌 Zones de disponibilité (AZ)
- Datacenters indépendants dans une même région.  
- Indépendance → alimentation, refroidissement, réseau.  
- Connectés par fibre privée ultra-rapide.  
- Utilisation → VM, disques, Load Balancer, bases SQL.  

**Catégories de services** :  
1. **Zonaux** (ex : VM épinglée dans une zone).  
2. **Redondants interzones** (ex : stockage ZRS, SQL Database).  
3. **Non régionaux** (ex : Traffic Manager).  

⚠️ Toutes les régions ne supportent pas les AZ.  

### 📌 Paires de régions
- Chaque région associée à une autre dans la même zone géographique (≥ 480 km).  
- Objectif : **résilience inter-région** (catastrophes, pannes).  
- Avantages :  
  - Restauration prioritaire en cas de panne massive.  
  - Mises à jour déployées une région à la fois.  
  - Données restent dans la même zone géographique (sauf exceptions).  

### 📌 Régions souveraines
- Instances **isolées** pour besoins légaux/conformité.  
- Exemples :  
  - **US Gov Cloud** (agences gouvernementales US).  
  - **Chine (21Vianet)** géré par un partenaire local.  

---

## 🗂️ 2. Infrastructure de gestion

### 📌 Ressources & groupes de ressources
- **Ressource** = unité de base (VM, VNet, base de données, etc.).  
- **Groupe de ressources (RG)** = conteneur logique.  
  - Une ressource = **un seul RG**.  
  - Actions au niveau RG s’appliquent à toutes les ressources (supprimer, accès, etc.).  
  - Organisation flexible : par **projet, environnement, accès**.  

### 📌 Abonnements
- Unité de **gestion, facturation, quotas**.  
- Lié à un **compte Azure (Entra ID)**.  
- Un compte peut avoir plusieurs abonnements.  

**Deux types de limites :**  
1. **Facturation** → facture séparée par abonnement.  
2. **Contrôle d’accès** → politiques & RBAC appliqués par abonnement.  

📌 Scénarios :  
- Séparer dev/test/prod.  
- Séparer par organisation ou facturation.  

### 📌 Groupes d’administration
- Niveau au-dessus des abonnements.  
- Sert à gérer **politiques, accès et conformité à grande échelle**.  
- Tout ce qui est appliqué au groupe est **hérité** par les abonnements, RG et ressources en dessous.  

**Caractéristiques :**  
- Jusqu’à **10 000 groupes** par annuaire.  
- Hiérarchie jusqu’à **6 niveaux de profondeur** (hors racine & abonnement).  
- Chaque groupe/abonnement = **un seul parent**.  

### 📌 Hiérarchie globale
```

Groupes d’administration
└── Abonnements
└── Groupes de ressources
└── Ressources

```

---

## 📊 3. Résumé du module
- **Centres de données** regroupés en **régions** et **zones de disponibilité**.  
- **Paires de régions** = réplication et continuité inter-régions.  
- **Régions souveraines** = isolées pour légalité/conformité.  
- **Ressources** organisées dans **groupes de ressources**.  
- **Abonnements** = unité de facturation et d’accès.  
- **Groupes d’administration** = niveau supérieur pour la gouvernance multi-abonnements.  

---

# 📝 Quiz d’entraînement – Infrastructure Azure

### Q1. Quelle est la relation entre une **zone de disponibilité** et une **région** ?
a) Une région contient plusieurs zones de disponibilité.  
b) Une zone contient plusieurs régions.  
c) Une zone et une région sont identiques.  
d) Une région = un seul datacenter toujours.  

---

### Q2. Quel avantage principal offrent les **paires de régions** ?  
a) Réduction des coûts de VM.  
b) Réplication et restauration en cas de panne régionale.  
c) Achat de domaines DNS.  
d) Gestion centralisée des ressources.  

---

### Q3. Une ressource Azure peut appartenir à :  
a) Plusieurs groupes de ressources en même temps.  
b) Un seul groupe de ressources à la fois.  
c) Aucun groupe de ressources.  
d) Plusieurs abonnements simultanément.  

---

### Q4. Quel est le rôle principal d’un **abonnement Azure** ?  
a) Héberger uniquement des machines virtuelles.  
b) Fournir une unité de facturation et de gestion d’accès.  
c) Séparer les régions souveraines.  
d) Permettre le peering entre réseaux virtuels.  

---

### Q5. Les **groupes d’administration** permettent :  
a) D’acheter de nouvelles régions.  
b) De gérer et appliquer des stratégies sur plusieurs abonnements.  
c) De créer des ressources physiques.  
d) D’ajouter de nouvelles zones de disponibilité.  

---

# ✅ Correction

- **Q1** → a  
- **Q2** → b  
- **Q3** → b  
- **Q4** → b  
- **Q5** → b  

---

