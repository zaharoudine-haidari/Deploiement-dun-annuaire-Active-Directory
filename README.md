# creation et mise en place d'un n'annuaire active directory


# Projet Active Directory

## 📌 Contexte
Ce projet a pour objectif de **concevoir, installer et configurer un annuaire Active Directory** dans un environnement Windows Server.  
L’exercice est réalisé dans un cadre d’apprentissage, avec une mise en situation professionnelle : mise en place d’un système d’authentification et de gestion des accès pour une entreprise bancaire fictive.

---

## 🎯 Objectifs du projet
- Installer et configurer **Windows Server + Active Directory** sur une machine virtuelle.
- Créer une **forêt, un domaine et des OU (Unités Organisationnelles)**.
- Définir et appliquer une **stratégie de gestion des droits d’accès**.
- Intégrer des **postes clients** au domaine.
- Démontrer un **cas pratique d’utilisation en entreprise** (gestion des accès par rôles et métiers).
- Développer des **scripts d’administration** pour améliorer la sécurité et la supervision.

---

## 🏦 Cas pratique : Banque fictive
L’organisation testée est une banque (nom fictif : *Crédit Industriel*).  
Le système d’accès est basé sur la **catégorisation des utilisateurs** :

- **Catégorie A – Guichetiers**  
  ➝ Peuvent uniquement transmettre des opérations, pas d’intervention.  

- **Catégorie B – Conseillers privés**  
  ➝ Opérations jusqu’à 10 000 €.  

- **Catégorie C – Gestionnaires et conseillers pro**  
  ➝ Opérations jusqu’à 100 000 €, avec validation supérieure.  

- **Catégorie D – Dirigeants, experts-comptables, DRH**  
  ➝ Accès complet.  

- **Clients**  
  ➝ Lecture seule de leur compte.  

- **Informatique & prestataires**  
  ➝ Lecture et exécution, pas d’écriture.  

- **Chefs de projet métier**  
  ➝ Modification illimitée dans les applications.

---

## 🖥️ Implémentation technique
### Étapes principales
1. **Installation de Windows Server** (VMware/VirtualBox).  
2. **Ajout du rôle Active Directory Domain Services (AD DS)**.  
3. **Configuration d’une IP fixe et du domaine**.  
4. **Création d’une forêt et des OU** correspondant aux catégories d’utilisateurs.  
5. **Ajout des utilisateurs internes et externes** :
   - Catégorie A : Amélie Lotte, Arthur Neutron
   - Catégorie B : Bob Voulet, Bruno Desange
   - Catégorie C : Céline Stoner, Cyril Potet
   - Catégorie D : Dorian Matias, Bernard Taperio (expert-comptable)
   - Clients : Karim Fed, Césarine Cordonnier
6. **Création des postes clients** et rattachement au domaine.  
7. **Vérification des accès et droits** selon la matrice définie.  

---

## 🔐 Sécurité et automatisation
Mise en place de scripts pour :  
- Identifier les **comptes inactifs**.  
- Détecter les **doublons d’utilisateurs**.  
- Générer une **alerte en cas de connexions suspectes** (ex. après certaines heures).  
- Suivre les **modifications sensibles** (≥ 3 modifications dans la même journée).  

Idées complémentaires :  
- Utilisation de **GPO (Group Policy Objects)** pour renforcer la sécurité.  
- Mise en place de **sauvegardes régulières** de l’annuaire.  
- Surveillance avec un outil de **SIEM** pour les logs de sécurité.  

---

## 📂 Compétences mises en avant
- Administration Windows Server  
- Gestion Active Directory (forêt, domaines, OU, utilisateurs, groupes)  
- Mise en place d’un **PAM (Privilege Access Management)**  
- Sécurité des systèmes et gestion des accès  
- Virtualisation (VMware / VirtualBox)  

---

## 🚀 Conclusion
Ce projet démontre la mise en place complète d’un environnement Active Directory, adapté à une organisation professionnelle fictive.  
Il met en avant la capacité à **administrer un SI, gérer les accès, automatiser des tâches et renforcer la sécurité**.
