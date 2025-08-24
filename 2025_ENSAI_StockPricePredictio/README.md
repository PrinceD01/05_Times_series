# 2025_ENSAI_StockPricePrediction  
*Prédiction du prix des actions NVIDIA avec méthodes de séries temporelles*

---

## 1. Objectifs du projet
- **Objectif principal** : Développer des modèles de prévision des prix de l’action NVIDIA (NVDA) à partir de données historiques (2010–2024), en testant des approches statistiques et de deep learning.  
- **Intérêt pédagogique** : Montrer les étapes clés d’un projet de séries temporelles, depuis le nettoyage des données jusqu’à la mise en place d’un outil interactif pour visualiser les prédictions.

---

## 2. Structure du projet

├── notebooks/
│   └── ProjetSerieTemporelle_Prince&Valdes.ipynb                   # Main Jupyter notebook with analysis
│
├── outputs/                                                        # Generated outputs folder
│
├── reports/
│   └── Rapport_ProjetSerieTemporelle_Prince&Valdes.pdf             # Project report
│
├── streamlit/
│   └── streamlit_app.py                                            # Streamlit web application
│
├── visualisations/                                                 # Generated visualizations
│   ├── Stock price prediction with GARCH model.png
│   ├── Stock price prediction with LSTM model - zoomed view.png
│   ├── Stock price prediction with LSTM model.png
└── └── Summary of performances model.png



---

## 3. Jeu de données
- **Source** : Yahoo Finance (API `yfinance`)  
- **Période** : 2010 – 2024  
- **Variables principales** :  
  - Date, Open, High, Low, Close, Volume  
- **Variable cible** : `Close` (prix de clôture de l’action NVIDIA)

---

## 4. Méthodologie
1. **Collecte des données** : Extraction des cours historiques depuis Yahoo Finance.  
2. **Prétraitement** : Nettoyage, transformation en séries temporelles, création d’indicateurs techniques (moyennes mobiles, RSI).  
3. **Analyse exploratoire** : Étude des tendances, saisonnalités, stationnarité (test ADF), décomposition.  
4. **Modélisation multi-approches** :  
   - **ARIMA** : modèle classique de séries temporelles *(testé mais peu performant ici)*.  
   - **GARCH** : pour la volatilité des rendements financiers.  
   - **LSTM bidirectionnel** : réseau de neurones récurrent pour capter les dépendances temporelles complexes.  
5. **Entraînement et validation** : Séparation Train (96%) / Test (4%), tuning d’hyperparamètres.  
6. **Évaluation** : Comparaison avec MSE, RMSE et MAE.  
7. **Déploiement** : Application **Streamlit** pour visualiser les prédictions et comparer avec les données réelles.

---

## 5. Livrables
- **Notebook d’analyse** : exploration et modélisation  
- **Visualisations** : tendances, décompositions, prédictions vs réelles  
- **Métriques** : MSE, RMSE, MAE pour comparer les modèles  
- **Modèles entraînés** : sauvegardes ARIMA, GARCH et LSTM  
- **Application Streamlit** : interface interactive de prédiction  

---

**Technologies utilisées** : Python, yfinance, statsmodels, ARCH, PyTorch, scikit-learn, matplotlib, Streamlit  
