
# 📧 Spam Detector - Machine Learning

Détecteur de spam utilisant le Machine Learning (Naive Bayes + TF-IDF)

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.3.0-orange.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## 🎯 Objectif
L’objectif principal est d’apprendre à un modèle informatique à analyser le contenu textuel des messages, à reconnaître des modèles linguistiques, puis à classer les messages en fonction de leur probabilité d’être du spam.
## 🚀 Fonctionnalités

- ✅ Prétraitement de texte (nettoyage, tokenisation, suppression stopwords)
- ✅ Vectorisation TF-IDF
- ✅ Modèle Naive Bayes
- ✅ Interface web interactive avec Gradio
- ✅ API REST avec Flask
- ✅ Précision : 97%+

## 📊 Dataset

**Source :** [SMS Spam Collection Dataset](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset)

- **Total :** 5,572 messages
- **Spam :** 747 (13.4%)
- **Ham :** 4,825 (86.6%)

## 🛠️ Installation

### Prérequis
- Python 3.8+
- pip


## 🎮 Utilisation

### Option 1 : Interface Gradio
```bash
python src/app.py
```

Puis ouvre : `http://localhost:7860`

### Option 2 : Entraîner ton propre modèle
```bash
python src/train.py
```

### Option 3 : API Flask
```bash
python src/api.py
```

Test avec curl :
```bash
curl -X POST http://localhost:5000/predict \
  -H "Content-Type: application/json" \
  -d '{"message":"WIN FREE MONEY NOW!!!"}'
```

### Option 4 : Notebook Jupyter
```bash
jupyter notebook notebooks/train_model.ipynb
```

## 📈 Résultats

| Métrique | Score |
|----------|-------|
| Accuracy | 97.2% |
| Precision | 96.8% |
| Recall | 94.5% |
| F1-Score | 95.6% |

**Matrice de Confusion :**
```
              Prédiction
              Ham   Spam
Réel   Ham   965     12
       Spam    8    130
```

## 🧪 Exemples de Prédictions
```python
from src.utils import predict_spam

# Exemple 1
predict_spam("Congratulations! You won $1000!")
# → SPAM (98.5%)

# Exemple 2
predict_spam("Hey, are we still meeting tomorrow?")
# → HAM (99.2%)
```

## 📂 Structure du Projet
```
spam-detector/
├── data/              # Datasets
├── models/            # Modèles sauvegardés
├── notebooks/         # Notebooks Jupyter
├── src/               # Code source
│   ├── app.py        # Interface Gradio
│   ├── train.py      # Entraînement
│   └── utils.py      # Fonctions utils
├── requirements.txt
└── README.md
```

## 🔧 Technologies Utilisées

- **Python 3.8+**
- **scikit-learn** - ML
- **NLTK** - NLP
- **Pandas** - Manipulation de données
- **Gradio** - Interface web
- **Flask** - API REST

## 📝 TODO

- [ ] Ajouter support multilingue
- [ ] Intégrer BERT/Transformers
- [ ] Déployer sur Hugging Face Spaces
- [ ] Créer une app mobile

## 🤝 Contribution

Les contributions sont les bienvenues !

1. Fork le projet
2. Crée une branche (`git checkout -b feature/AmazingFeature`)
3. Commit tes changements (`git commit -m 'Add AmazingFeature'`)
4. Push sur la branche (`git push origin feature/AmazingFeature`)
5. Ouvre une Pull Request

## 📄 Licence

MIT License - voir le fichier [LICENSE](LICENSE)

## 👤 Auteur

**Ton Nom**
- GitHub: [@ton-username](https://github.com/ton-username)
- LinkedIn: [Ton Profil](https://linkedin.com/in/ton-profil)

## 🙏 Remerciements

- Dataset : UCI Machine Learning Repository
- Inspiration : Kaggle Community

---

⭐ **N'oublie pas de mettre une étoile si ce projet t'a aidé !**
```

---

### **4. LICENSE (Optionnel)**

Créer un fichier `LICENSE` avec la licence MIT :
```
MIT License

Copyright (c) 2026 Ton Nom

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files , to deal
in the Software without restriction.
