# 🚛 Projet SD-VRP - Optimisation des Livraisons avec Livraisons Fractionnées

![Banner](./summary graph.pdf)  
*Résumé visuel des performances (voir [Summary_Graph.pdf](./Summary_Graph.pdf))*


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
```python
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
