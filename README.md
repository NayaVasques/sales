# Prédiction des Ventes avec Machine Learning

## **1. Introduction**
Dans le cadre de ce projet, nous avons développé un modèle de Machine Learning permettant de prévoir les ventes futures des magasins à partir de données historiques. L'objectif principal est d'aider les gestionnaires à optimiser leurs stratégies de vente en identifiant les facteurs influençant les performances.

## **2. Exploration des Données**
Avant de développer les modèles, nous avons procédé à une analyse approfondie des données :

### **Problèmes et Solutions**
- **Données manquantes :** Aucun problème critique, les valeurs manquantes étaient insignifiantes.
- **Données redondantes :** Nettoyage effectué pour éviter la multi-colinéarité.
- **Transformation des variables :** Encodage One-Hot pour les variables catégoriques (régions, catégories de produits).

### **Insights Clés**
- Les **remises ont un fort impact négatif sur les profits** mais augmentent les ventes.
- Certains **mois et certaines régions montrent une forte saisonnalité**.
- Les **produits et catégories influencent directement les performances des magasins**.

**💡 Améliorations possibles :**
- **Explorer comment la saisonnalité, les catégories de produits et les régions interagissent entre elles.**
- **Analyser les relations entre discounts, régions et ventes pour mieux comprendre les décisions stratégiques.**

## **3. Approche Machine Learning**
### **Modèles Testés**
Trois modèles ont été testés pour identifier celui offrant les meilleures prédictions :
- **Régression Linéaire** (baseline simple)
- **Random Forest** (meilleur compromis performance/interprétabilité)
- **XGBoost** (puissant pour la modélisation des données complexes)

### **Comparaison des Performances**
| Modèle            | MAE (Erreur Absolue Moyenne) | RMSE (Erreur Quadratique Moyenne) |
|-------------------|--------------------------|---------------------------------|
| Régression Linéaire | 202.26                    | 346.98                          |
| Random Forest    | **91.33**                 | **233.64**                      |
| XGBoost         | 99.02                     | 233.75                          |

**✅ Choix final : Random Forest, offrant les meilleurs résultats.**

## **4. Déploiement et Amélioration**
### **Suivi et Maintenance du Modèle**
- **Détection des dérives du modèle** : Réentraînement régulier.
- **Mise à jour des données** : Adaptation aux nouvelles tendances de ventes.
- **Optimisation continue** : Ajustement des hyperparamètres si nécessaire.

## **5. Instructions pour Exécution**
### **Prérequis**
- Python 3.x
- Bibliothèques requises : `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `xgboost`

### **Installation des Dépendances**
```bash
pip install -r requirements.txt
```

### **Exécution du Projet**
1. **Charger les données** dans le fichier `stores_sales_forecasting.csv`.
2. **Lancer le script** principal :
   ```bash
   python moovai_test.py
   ```
3. **Explorer les résultats** : performances du modèle et insights affichés.

---
**Projet réalisé dans le cadre d'un test technique en Data Science.**

