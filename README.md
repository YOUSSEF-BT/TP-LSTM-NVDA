# TP — Prédiction du cours de NVIDIA (NVDA) avec LSTM

## 1) À propos
Ce dépôt contient un **TP réalisé en cours avec le professeur**.  
➡️ **Ce n’est pas un projet personnel**, mais un travail pédagogique (exercice académique).

---

## 2) Fichiers du dépôt
- `LTSM_Scraping_Nvdia.ipynb` : le notebook du TP (chargement des données, préparation, entraînement LSTM, graphiques).
- `NVDIA_historical_data.csv` : dataset utilisé par le notebook (données historiques de NVIDIA).

---

## 3) Dataset — `NVDIA_historical_data.csv`
### Description
Le fichier contient une série temporelle boursière pour NVIDIA (NVDA), avec les colonnes suivantes :
- `Date`
- `Open` (ouverture)
- `High` (plus haut)
- `Low` (plus bas)
- `Close` (clôture)
- `Volume`

**Période des données :** du `2020-11-20` au `2025-11-19`.

### Important (format du CSV)
Le CSV contient **3 lignes d’en-tête** (métadonnées).  
Si tu le lis directement avec `pandas`, utilise `skiprows=3`.

Exemple :

```python
import pandas as pd

df = pd.read_csv(
    "NVDIA_historical_data.csv",
    skiprows=3,
    names=["Date", "Close", "High", "Low", "Open", "Volume"]
)

df["Date"] = pd.to_datetime(df["Date"])
df = df.sort_values("Date")
df.head()
```

4) Ce que fait le TP (résumé clair)

Charge les données (depuis le CSV)

Prépare la série temporelle (ex: normalisation + création de fenêtres temporelles)

Entraîne un modèle LSTM

Affiche des graphiques et compare valeurs réelles vs prédictions

5) Exécution

Option A — Google Colab (le plus simple)

Ouvre LTSM_Scraping_Nvdia.ipynb dans Colab

Upload NVDIA_historical_data.csv dans Colab (même dossier)

Exécute les cellules dans l’ordre

Option B — En local (Jupyter)

Installer Jupyter :

pip install notebook

Lancer :

jupyter notebook

Ouvrir LTSM_Scraping_Nvdia.ipynb et exécuter les cellules

6) Dépendances (typiques)

Selon le notebook, tu peux avoir besoin de :

numpy, pandas, matplotlib

scikit-learn

tensorflow / keras

Installation (générale) :

pip install numpy pandas matplotlib scikit-learn tensorflow

7) Notes

Travail pédagogique uniquement : ce n’est pas un conseil financier.

Les résultats varient selon les hyperparamètres (fenêtre temporelle, epochs, batch size, etc.).

8) Auteur

Youssef BT — TP réalisé en cours avec le professeur (non personnel)
