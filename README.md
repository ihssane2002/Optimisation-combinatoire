# 🚛 Projet SD-VRP - Optimisation des Livraisons avec Livraisons Fractionnées
##  Summary Graph

[![Visualisation des Résultats](https://img.shields.io/badge/View-Summary_Graph-blue?style=for-the-badge&logo=adobe-acrobat-reader)](summary%20graph.pdf)

*Cliquez sur le bouton ci-dessus pour visualiser le poster du projet complet*


## 📌 Description du Projet
**Problème** : Le SD-VRP (Split Delivery Vehicle Routing Problem) étend le problème classique de tournées de véhicules en permettant à un client d'être servi par plusieurs véhicules.

**Objectifs** :
- Minimiser le coût total des tournées
- Satisfaire toutes les demandes clients
- Respecter les capacités des véhicules

**Applications** :
- Livraisons urbaines
- Logistique alimentaire
- Gestion de flottes

---
## 🛠️ Méthodologie
### 1. Approche Exacte (Solveur PuLP/CBC)
 Variables :
 x[i,j,k] = 1 si le véhicule k voyage de i à j
 y[i,k] = quantité livrée au client i par le véhicule k

### 2. Métaheuristique (Algorithme Tabou)
 Paramètres :
- Taille liste tabou : 50
- Itérations maximales : 1000

## 🚀 Utilisation du Projet

1. Installation

git clone https://github.com/ihssane2002/Optimisation-combinatoire.git
cd Optimisation-combinatoire

2. Exécution
Solveur Exact :

jupyter notebook Code/Solveur/Case0.ipynb

Métaheuristique :

python Code/Metaheuristique/tabu_search.py --instance Case10

# 📄 Conclusion 
Bilan
Le solveur excelle sur les petites instances (<70 clients)

L'algorithme tabou fournit des solutions viables pour tous les cas
