# Brahim IT Lab 🧪💻

Laboratoire personnel d'apprentissage en **administration systèmes, réseau et support informatique**.

Ce projet simule l’infrastructure informatique d’une petite entreprise afin de pratiquer des situations réelles de **support IT** et d’**administration systèmes**.

L’objectif est simple : **apprendre en construisant, casser des choses, réparer, documenter et recommencer.**

---

# 🎯 Objectifs du projet

Ce laboratoire sert à développer des compétences concrètes :

🖥️ **Support utilisateurs**
- diagnostic d'incidents
- résolution de problèmes
- procédures de dépannage

🗄️ **Administration systèmes**
- gestion d’utilisateurs
- gestion des permissions
- gestion de serveurs

🌐 **Réseau**
- DNS
- DHCP
- communication client / serveur

⚙️ **Virtualisation**
- création de machines virtuelles
- snapshots
- tests d'infrastructure

📚 **Documentation technique**
- procédures
- incidents
- journal de bord

---

# 🖥️ Environnement technique

Tout le laboratoire tourne sur **un seul PC personnel**.

**Machine hôte**

- Linux Bazzite 🐧

**Technologies utilisées**

- Virtualisation
- Git / GitHub
- Markdown
- Linux
- Windows Server

---

# 🏢 Architecture simulée

Le laboratoire reproduit une petite infrastructure d'entreprise.


# Journal de bord – Brahim IT Lab 🧪💻

## 06/03/2026 🚀

Aujourd'hui, on a rencontré nos **premiers défis Git** ! 💡  

### Problème 1 : Authentification avec GitHub 🔑

En voulant pousser mon fichier `JOURNAL.md` :

git push origin main

Git m’a répondu :

remote: Invalid username or token
fatal: Authentication failed

➡️ Cause : GitHub n’accepte plus les mots de passe classiques. Mon token (PAT) initial avait été exposé et a été révoqué.

Solution :

Supprimer le token compromis sur GitHub

Générer un nouveau Personal Access Token avec la permission repo ✅

Configurer le remote proprement, sans inclure le token dans l’URL :

git remote set-url origin https://github.com/BrahimZiyani/Brahim-IT-Solutions.git

Utiliser le token comme mot de passe lors du push

Résultat : push réussi ! 🎉

### Problème 2 : Branches divergentes 🔄

Push rejeté : non-fast-forward.
Cause : le dépôt distant contenait déjà un commit (README initial).

Solution :

git pull --rebase origin main

Résoudre les éventuels conflits (ici aucun)

git push origin main
✅ Historique propre et synchronisé

Apprentissages du jour :

Sécuriser les tokens 🔐

--rebase garde un historique linéaire 📈
