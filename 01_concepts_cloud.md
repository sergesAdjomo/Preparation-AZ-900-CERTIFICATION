# ☁️ Concepts du Cloud Computing – Résumé

---

## 📌 Qu’est-ce que le cloud computing ?
- Fourniture de **services informatiques via Internet** : VM, stockage, bases de données, réseaux, IoT, ML, IA…  
- Permet d’augmenter rapidement l’infrastructure **sans construire de datacenter**.  
- Évolutif, flexible et basé sur la demande.  

---

## 🔑 Modèle de responsabilité partagée
- Dans un **datacenter classique** → l’entreprise gère **tout** (physique + logiciel).  
- Dans le **cloud** → responsabilités partagées entre le fournisseur et le client.  

**Toujours fournisseur** : sécurité physique, alimentation, réseau, hôtes physiques.  
**Toujours client** : données, identités, appareils, accès.  
**Dépend du modèle** : OS, middleware, applications.  

- **IaaS** → + de responsabilités côté client.  
- **PaaS** → responsabilités partagées.  
- **SaaS** → + de responsabilités côté fournisseur.  

---

## 🌍 Modèles de cloud
1. **Cloud privé** : réservé à une seule organisation (contrôle élevé, coûts plus élevés).  
2. **Cloud public** : ressources partagées via un fournisseur cloud (Azure, AWS, GCP).  
3. **Cloud hybride** : combinaison privé + public, interconnectés.  
4. **Multicloud** : plusieurs fournisseurs publics utilisés en parallèle.  

### Outils associés
- **Azure Arc** → gérer hybride/multicloud.  
- **Azure VMware Solution** → migrer charges VMware vers Azure.  

---

## 💰 Modèle basé sur la consommation
- **CapEx** = investissements initiaux (achat datacenter, matériel…).  
- **OpEx** = dépenses d’exploitation (abonnement cloud, leasing, etc.).  
- Le cloud = **OpEx**, paiement **à l’usage**.  

**Avantages** :  
- Pas de frais initiaux.  
- Paiement uniquement des ressources consommées.  
- Elasticité → scale up/down rapide.  
- Pas de surcapacité ni sous-capacité comme en datacenter classique.  

---

## 💵 Modèles tarifaires du cloud
- **Pay-as-you-go (PAYG)** → paiement selon usage réel (flexible, agile).  
- **Reserved Instances / Réservations** → engagement (1 à 3 ans) → réduction des coûts.  
- **Spot instances** → prix réduit, mais résiliation possible si besoin de capacité par Azure.  

---

# 📝 Quiz d’entraînement – Concepts Cloud

### Q1. Quel est le principal avantage du cloud computing par rapport à un datacenter classique ?  
a) Coûts initiaux plus élevés  
b) Scalabilité rapide et paiement à l’usage  
c) Nécessité d’acheter du matériel  
d) Maintenance physique par le client  

---

### Q2. Dans le modèle de responsabilité partagée, qui est **toujours responsable des données** ?  
a) Le fournisseur cloud  
b) Le client  
c) Les deux  
d) Personne  

---

### Q3. Quel modèle de cloud permet d’avoir à la fois un environnement privé et public interconnecté ?  
a) Public  
b) Privé  
c) Hybride  
d) Multicloud  

---

### Q4. Le modèle CapEx correspond à :  
a) Abonnement cloud mensuel  
b) Investissement initial dans des ressources tangibles  
c) Location d’un centre de convention  
d) Paiement à l’usage  

---

### Q5. Quel outil Azure permet de gérer un environnement hybride ou multicloud ?  
a) Azure Functions  
b) Azure Arc  
c) Azure Monitor  
d) Azure VMware Solution  

---

# ✅ Correction
- **Q1** → b  
- **Q2** → b  
- **Q3** → c  
- **Q4** → b  
- **Q5** → b  

---
