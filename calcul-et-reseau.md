# 📘 Révisions AZ-900 – Calcul & Réseau Azure

---

## 🌍 Présentation du module
- **Options de calcul** : Machines virtuelles (VMs), Conteneurs, Fonctions.  
- **Fonctionnalités réseau** : VNets, Azure DNS, Azure ExpressRoute.  

### Objectifs
- Comparer VM, conteneurs, fonctions.  
- Décrire options de VM (VM, VMSS, Availability Sets, AVD).  
- Décrire ressources nécessaires à une VM.  
- Expliquer options d’hébergement (App Service, conteneurs, VMs).  
- Décrire mise en réseau (VNets, sous-réseaux, DNS, VPN Gateway, ExpressRoute).  
- Différencier endpoints publics/privés.  

---

## 💻 Machines virtuelles Azure
- Service **IaaS**, contrôle total sur l’OS et logiciels.  
- Création rapide via **images** (préconfigurées).  
- Cas d’usage :  
  - Dev/Test  
  - Hébergement d’applications  
  - Extension datacenter  
  - Récupération d’urgence  
  - Migration « lift-and-shift »  

### Mise à l’échelle
- **VMSS (Virtual Machine Scale Sets)** → autoscaling, load balancing.  
- **Availability Sets** → tolérance aux pannes :  
  - Update domains (mises à jour étalées).  
  - Fault domains (sources d’alimentation/réseaux différents).  

### Ressources d’une VM
- Taille (CPU, RAM).  
- Stockage (HDD, SSD).  
- Réseau (VNet, IP publique, ports).  

---

## 🔒 Réseaux privés virtuels (VPN)
- **Tunnel chiffré** sur Internet.  
- Passerelle VPN (1 par VNet) → permet :  
  - Site-to-site  
  - Point-to-site  
  - VNet-to-VNet  
- Types :  
  - **Policy-based** → adresses IP statiques.  
  - **Route-based** (par défaut) → plus flexible (requis pour VNet-to-VNet, P2S, multisite, ExpressRoute coexistence).  

### Haute dispo
- **Actif/Passif** → bascule automatique.  
- **Actif/Actif (BGP)** → tunnels multiples.  
- **Basculement ExpressRoute** → secours en cas de panne.  
- **Redondance interzones** → tolérance accrue (zones Azure).  

---

## ⚡ Azure ExpressRoute
- Connexion **privée** (ne passe pas par Internet).  
- Avantages : plus **sécurisé, fiable, rapide** (latence constante).  
- **Accès direct** à Azure, Microsoft 365, Dynamics 365.  
- **BGP** pour routage dynamique.  
- **Global Reach** → interconnecter plusieurs sites via réseau Microsoft.  

### Modèles de connectivité
1. Colocation CloudExchange  
2. Ethernet point-à-point  
3. Any-to-Any (WAN ↔ Azure)  
4. Direct (peering Microsoft, 10/100 Gbps Active/Active)  

---

## 🌐 Azure DNS
- Service de **résolution de noms** basé sur Azure.  
- Avantages : fiabilité, sécurité (RBAC, logs, locks), simplicité.  
- Gère DNS publics et **privés** (zones DNS privées pour VNets).  
- **Alias records** → lient à ressources Azure (IP publique, Traffic Manager, CDN), maj auto si IP change.  
- ⚠️ Ne permet pas d’acheter un domaine (passer par App Service Domain ou registrar externe).  

---

## 📊 Résumé du module
- **Calcul** : VMs, Conteneurs, Fonctions.  
- **VMSS, Availability Sets, AVD** → scalabilité + haute dispo.  
- **App Service** → hébergement simple.  
- **Réseau** : VNets, Subnets, Peering, DNS, VPN Gateway, ExpressRoute.  
- **Endpoints publics/privés** = contrôle de l’accès.  

---

# 📝 Quiz d’entraînement

### Q1. Quels sont les cas d’usage typiques des machines virtuelles Azure ?  
a) Tests/Développement  
b) Hébergement d’applications  
c) Migration lift-and-shift  
d) Achat de domaines  

---

### Q2. Quelle différence entre Policy-based VPN et Route-based VPN ?  
a) Policy-based = adresses IP statiques / Route-based = routage dynamique  
b) Policy-based = routage BGP / Route-based = pas de routage  
c) Policy-based = haute dispo / Route-based = uniquement dev/test  

---

### Q3. ExpressRoute offre…  
a) Connexion via Internet public  
b) Connexion privée, rapide et sécurisée  
c) Connexion uniquement aux VM Azure  
d) Achat direct de noms de domaine  

---

### Q4. Quels avantages clés d’Azure DNS ?  
a) RBAC et journaux d’activité  
b) Alias records auto-mis à jour  
c) Achat de domaines inclus  
d) Zones DNS privées  

---

### Q5. Que fait un Availability Set ?  
a) Crée plusieurs VM identiques à charge équilibrée  
b) Répartit les VM sur update/fault domains pour tolérance aux pannes  
c) Permet d’acheter un domaine directement dans Azure  
d) Connecte deux VNets entre eux  

---

# ✅ Correction du Quiz

- **Q1** → a, b, c  
- **Q2** → a  
- **Q3** → b  
- **Q4** → a, b, d  
- **Q5** → b  

---
