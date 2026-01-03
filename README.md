# TP — Prédiction du cours de NVIDIA (NVDA) avec LSTM

## À propos
Ce dépôt contient un **TP réalisé en cours avec le professeur**.  
➡️ **Ce n’est pas un projet personnel**, mais un travail pédagogique.

---

## Contenu du dépôt
- **Notebook (.ipynb)** : le TP complet (chargement des données, préparation, entraînement LSTM, graphiques).
- **Dataset** : `NVDIA_historical_data.csv`  
  Données historiques de l’action **NVIDIA (NVDA)** utilisées dans le notebook.

---

## Dataset — `NVDIA_historical_data.csv`
Ce fichier contient des données boursières (série temporelle).  
En général, on y retrouve les colonnes suivantes :
- `Date` : date
- `Open` : prix d’ouverture
- `High` : plus haut
- `Low` : plus bas
- `Close` : prix de clôture
- `Volume` : volume échangé

> Remarque : selon la source d’export, le CSV peut parfois contenir des lignes d’en-tête/métadonnées en haut.  
> Si tu as une erreur de lecture, adapte le chargement dans le notebook (ex: `skiprows`).

---

## Comment exécuter
### Option 1 — Google Colab (simple)
1. Ouvre le fichier **.ipynb** dans Colab
2. Assure-toi que `NVDIA_historical_data.csv` est dans le même dossier (ou upload-le dans Colab)
3. Exécute les cellules dans l’ordre

### Option 2 — En local (Jupyter)
1. Installe les dépendances
2. Lance Jupyter et ouvre le notebook

---

## Dépendances (typiques)
Le notebook utilise généralement :
- `numpy`, `pandas`, `matplotlib`
- `scikit-learn` (normalisation / split)
- `tensorflow` / `keras` (modèle LSTM)
- (optionnel) `yfinance` si les données sont téléchargées en ligne

---

## Ce que fait le TP (résumé clair)
1. **Charge** les données (CSV local et/ou téléchargement)
2. **Prépare** la série temporelle (ex: normalisation + création de fenêtres “timesteps”)
3. **Entraîne** un modèle **LSTM**
4. **Compare** prédictions vs valeurs réelles avec des graphiques

---

## Notes importantes
- Travail **pédagogique** uniquement : **pas un conseil financier**.
- Les résultats dépendent des hyperparamètres (fenêtre, epochs, batch size, etc.).

---

## Auteur
**Youssef BT** — TP réalisé **en cours avec le professeur** (non personnel)
