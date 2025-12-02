# 📊 Curs 2: Analiza Avansată de Date cu Python - Data Science Essentials

## 🎯 Overview

Acest curs introduce participanții în lumea **data science** folosind Python, pandas, și instrumente moderne de vizualizare. Vom lucra cu **date reale** de la Eurostat (EU-SILC) și vom învăța să folosim **AI assistants** pentru productivitate crescută.

**Durata:** 6 sesiuni × 1.5 ore = **9 ore total**
**Format:** Live coding, hands-on, proiecte practice
**Nivel:** Intermediar (necesită completarea Cursului 1)

---

## 📚 Sesiuni

| # | Titlu                                                  | Durată | Focus |
|---|--------------------------------------------------------|--------|-------|
| 1 | Recap & Pandas Intro                                   | 1.5h | Review + DataFrames basics |
| 2 | Loading and Cleaning Data with Pandas                  | 1.5h | Curățare date complexe |
| 3 | Exploratory Data Analysis (EDA) with Python            | 1.5h | Statistici & agregări |
| 4 | Data Visualization with Python                         | 1.5h | Matplotlib & Seaborn |
| 5 | More on data handling and data processing with Python/Working with Complex Data and Multiple Files | 1.5h | Excel, PDF, merge |
| 6 |Usage of LLMs for data science and learning Python                                 | 1.5h | ChatGPT & Claude |

---


## 🛠️ Setup Tehnic

### Cerințe:
- **Python 3.8+** (recomandat 3.9 sau 3.10)
- **Jupyter Notebook** sau **JupyterLab**
- **Biblioteci**: pandas, numpy, matplotlib, seaborn, openpyxl

### Instalare:

#### Opțiunea 1: pip (recomandat)
```bash
# Instalare biblioteci necesare
pip install pandas numpy matplotlib seaborn openpyxl jupyter

# Verificare instalare
python -c "import pandas; print(f'Pandas {pandas.__version__} instalat!')"
```

#### Opțiunea 2: Anaconda (include tot)
```bash
# Dacă aveți Anaconda instalat deja
conda install pandas numpy matplotlib seaborn openpyxl jupyter
```

#### Opțional (pentru Sesiunea 5 - PDF):
```bash
pip install pdfplumber tabula-py
```

### Verificare Setup:
Rulați acest test pentru a verifica că totul e instalat:
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

print("✅ Toate bibliotecile sunt instalate corect!")
print(f"Pandas: {pd.__version__}")
print(f"NumPy: {np.__version__}")
```

---

## 📊 Datasets Folosite

### 1. EU-SILC Estonia (Principal)
**Sursa:** [Eurostat Public Microdata](https://ec.europa.eu/eurostat/web/microdata/public-microdata/statistics-on-income-and-living-conditions)

**Despre:**
- Statistics on Income and Living Conditions
- Microdata anonimizată la nivel de gospodărie
- Date oficiale UE, relevante pentru Moldova
- ~2000-3000 records cu 50+ variabile

**Download:**
- Direct: [EE_PUF_EUSILC.zip](https://ec.europa.eu/eurostat/documents/203647/16979414/EE_PUF_EUSILC.zip/)
- Metadata: [Excel codebook](http://ec.europa.eu/eurostat/documents/203647/203704/EU+SILC+PUF+metadata/)
