# 📊 Temă 1 (Curs 1): Analiza Datelor Statistice Naționale

## 🎯 Obiective de Învățare

Prin completarea acestei teme, studenții vor:

### Competențe Tehnice:
- ✅ **Curăța date reale** - eliminarea inconsistențelor, tratarea valorilor lipsă
- ✅ **Manipula structuri de date** - liste și dicționare complexe
- ✅ **Crea funcții reutilizabile** - modularizarea codului
- ✅ **Aplica structuri de control** - if/elif/else, for, while
- ✅ **Calcula statistici** - medii, sume, extreme, top N
- ✅ **Grupa și filtra date** - organizarea informațiilor
- ✅ **Compara și clasifica** - analiză comparativă

### Competențe Analitice:
- 📊 Gândire statistică - interpretarea datelor
- 🧩 Descompunerea problemelor - împărțirea în pași mici
- 🔄 Compoziția funcțiilor - combinarea operațiilor simple
- 🎨 Prezentarea datelor - formatarea profesională a rezultatelor

---

## 📚 Structura Materialelor

### 1. **`homework_1_statistics_practice.ipynb`** - Notebook Principal
**Ce conține:**
- 10 regiuni cu date statistice realiste (Chișinău, Bălți, Cahul, etc.)
- 8 indicatori per regiune (populație, venit, ocupare, șomaj, etc.)
- Date "murdare" cu probleme reale (spații, None, inconsistențe)
- 15 exerciții progressive:
  - **Partea 1**: Date inițiale (vizualizare date murdare)
  - **Partea 2**: Curățarea datelor (4 exerciții)
  - **Partea 3**: Analiza datelor (11 exerciții)

**Pentru cine:** Toți studenții - exerciții practice de rezolvat

### 2. **`homework_1_solutions.ipynb`** - Soluții Complete
**Ce conține:**
- Soluții complet comentate pentru toate exercițiile
- Explicații pas cu pas pentru fiecare linie de cod
- Docstrings profesionale pentru fiecare funcție
- Exemple de output și teste
- Explicații conceptuale

**Pentru cine:**
- Studenți blocați - consultare după încercări proprii
- Profesori - verificare și evaluare
- Referință - învățare prin exemple

### 3. **`README.md`** - Acest Fișier
Documentație completă, ghid de utilizare, structură

---

## 🚀 Cum să Folosiți Aceste Materiale

### Pentru Studenți:

#### Pasul 1: Pregătire
```bash
# Asigurați-vă că aveți Python și Jupyter instalate
jupyter notebook
```

#### Pasul 2: Lucru la Exerciții
1. **Deschideți** `homework_1_statistics_practice.ipynb`
2. **Citiți** cerințele cu atenție
3. **Încercați** să rezolvați singur fiecare exercițiu
4. **Testați** funcțiile după ce le scrieți
5. **Debugging** - folosiți `print()` pentru a vedea ce se întâmplă

#### Pasul 3: Verificare
- **NU** deschideți soluțiile imediat!
- Încercați mai multe abordări dacă prima nu funcționează
- Consultați notebook-urile din Cursul 1 dacă aveți nevoie
- Doar când sunteți cu adevărat blocat, consultați soluțiile

#### Pasul 4: Învățare din Soluții
1. Comparați soluția voastră cu soluția oficială
2. Înțelegeți diferențele
3. Citiți comentariile pentru explicații
4. Încercați să rescrieți funcția în stilul vostru

### Pentru Profesori:

#### Predare:
1. **Demo live** - arătați primele 2-3 exerciții rezolvate
2. **Lucru individual** - lăsați studenții să lucreze
3. **Peer review** - studenții își verifică codul reciproc
4. **Discuții** - abordări diferite pentru aceeași problemă

#### Evaluare:
- **Corectitudinea** - funcțiile produc rezultate corecte?
- **Stilul de cod** - cod curat, comentat, ușor de citit?
- **Eficiența** - abordări optime?
- **Creativitate** - soluții inovative?

#### Timp Estimat:
- **Minimum**: 4-6 ore (exerciții de bază)
- **Complet**: 8-10 ore (toate exercițiile + bonus)
- **Optim pentru curs**: 2-3 sesiuni de 3 ore

---

## 📋 Conținut Detaliat

### Partea 1: Date Inițiale
**Concepte:** Structuri de date, vizualizare probleme

```python
# 10 regiuni moldovenești
# 8 indicatori fiecare
# Probleme intenționate:
- Spații extra: "Chișinău ", "  Cahul"
- Majuscule inconsistente: "servicii", "AGRICULTURĂ"
- Valori lipsă: None în rata_ocupare, venit_mediu, etc.
```

### Partea 2: Curățarea Datelor (Exercițiile 1-4)

| Ex | Funcție | Dificultate | Concepte |
|---|---|---|---|
| 1 | `curata_text()` | ⭐ | `.strip()`, `.title()` |
| 2 | `calculeaza_medie_camp()` | ⭐⭐ | Loop, condiții, None |
| 3 | `completeaza_valori_lipsa()` | ⭐⭐ | Modificare in-place |
| 4 | `curata_date_complete()` | ⭐⭐⭐ | Compoziție funcții |

### Partea 3: Analiza Datelor (Exercițiile 5-15 + Bonus)

| Ex | Funcție | Dificultate | Concepte |
|---|---|---|---|
| 5 | `afiseaza_regiune()` | ⭐ | Formatare string |
| 6 | `extrage_nume_regiuni()` | ⭐ | List comprehension |
| 7 | `calculeaza_statistici_nationale()` | ⭐⭐ | Agregări |
| 8 | `adauga_densitate_intreprinderi()` | ⭐⭐ | Câmpuri calculate |
| 9 | `filtreaza_regiuni_dezvoltate()` | ⭐⭐ | Filtrare multi-criteriu |
| 10 | `clasifica_regiune_dupa_populatie()` | ⭐⭐ | If-elif-else |
| 11 | `grupeaza_dupa_sector()` | ⭐⭐⭐ | Dicționare dinamice |
| 12 | `calculeaza_statistici_sector()` | ⭐⭐⭐ | Agregări selective |
| 13 | `gaseste_extreme()` | ⭐⭐ | Min/max manual |
| 14 | `top_regiuni()` | ⭐⭐⭐⭐ | Sortare (bubble sort) |
| 15 | `compara_regiuni()` | ⭐⭐⭐ | Comparație structurată |
| 🎁 | `genereaza_raport_complet()` | ⭐⭐⭐⭐⭐ | Compoziție totală |

---

## 💡 Sfaturi și Bune Practici

### Debugging:
```python
# Folosiți print() pentru a vedea ce se întâmplă
def functia_mea(lista):
    print(f"DEBUG: Am primit {len(lista)} elemente")
    for element in lista:
        print(f"DEBUG: Procesez {element}")
        # ... cod aici
```

### Testare Incrementală:
```python
# NU scrieți toată funcția deodată!
# Testați pas cu pas:

# Pas 1: Scrieți structura de bază
def calculeaza_ceva(lista):
    pass

# Pas 2: Adăugați prima parte
def calculeaza_ceva(lista):
    suma = 0
    print(f"Start: suma={suma}")  # TEST
    return suma

# Pas 3: Adăugați logica
def calculeaza_ceva(lista):
    suma = 0
    for element in lista:
        suma += element
        print(f"După {element}: suma={suma}")  # TEST
    return suma

# Pas 4: Curățați print-urile de test
def calculeaza_ceva(lista):
    suma = 0
    for element in lista:
        suma += element
    return suma
```

### Citirea Erorilor:
```python
# Eroare tipică:
# KeyError: 'populatie'

# Ce înseamnă?
# → Încercați să accesați o cheie care nu există
# → Verificați scrierea: "populatie" sau "populație"?
# → Verificați dicționarul: print(regiune.keys())
```

---

## 🎓 Criterii de Evaluare

### Nota 5-6 (Satisfăcător):
- ✅ Rezolvă exercițiile 1-7
- ✅ Funcțiile returnează rezultate corecte
- ✅ Cod funcțional (chiar dacă nu elegant)

### Nota 7-8 (Bine):
- ✅ Rezolvă exercițiile 1-12
- ✅ Cod curat, cu comentarii
- ✅ Folosește funcții componente

### Nota 9-10 (Excelent):
- ✅ Rezolvă TOATE exercițiile (inclusiv bonus)
- ✅ Cod profesional, bine comentat
- ✅ Abordări creative și eficiente
- ✅ Raportul final funcționează perfect

---

## 🔧 Cerințe Tehnice

### Software Necesar:
- **Python 3.7+** (recomandat 3.8 sau mai nou)
- **Jupyter Notebook** sau **JupyterLab**
- **Nicio bibliotecă externă** - doar Python standard library!

### Instalare:
```bash
# Verificați Python
python --version  # sau python3 --version

# Instalați Jupyter dacă nu îl aveți
pip install jupyter

# SAU folosiți Anaconda (include tot)
# https://www.anaconda.com/
```

### Structura Folderului:
```
homework_1/
├── README.md                              # Acest fișier
├── QUICK_START.md                         # Ghid rapid de start
├── homework_1_statistics_practice.ipynb   # Exerciții
├── homework_1_hints.ipynb                 # Structură și hint-uri
└── homework_1_solutions.ipynb             # Soluții complete
```

---

## 📖 Concepte Python Folosite

### Din Cursul 1:
- ✅ Variabile și tipuri de date
- ✅ Liste: append, indexing, slicing, iteration
- ✅ Dicționare: keys, values, items, dynamic keys
- ✅ Funcții: def, parametri, return, docstrings
- ✅ Condiționali: if, elif, else, operatori logici
- ✅ Bucle: for, while, range, enumerate
- ✅ String methods: .strip(), .title(), f-strings
- ✅ Operatori: aritmetici, comparație, logici
- ✅ None și verificarea valorilor

### Concepte Noi Aplicate:
- 🆕 Compoziția funcțiilor (funcții care folosesc alte funcții)
- 🆕 Modificare in-place vs. returnare copie
- 🆕 Dicționare cu chei dinamice
- 🆕 Agregări complexe (sume, medii, grupări)
- 🆕 Formatare avansată cu f-strings
- 🆕 Algoritmi simpli (găsire min/max, sortare)

---

## 🤝 Întrebări Frecvente (FAQ)

### 1. "Pot folosi biblioteci externe precum pandas?"
**NU!** Scopul este să învățați fundamentele Python. Pandas va fi în cursul următor.

### 2. "Cât timp ar trebui să dureze?"
**4-10 ore** în funcție de experiență. Nu vă grăbiți!

### 3. "Când să consult soluțiile?"
După ce ați încercat **serios** singur. Minim 30 min per exercițiu dificil.

### 4. "Ce fac dacă primesc erori?"
1. **Citiți mesajul** de eroare cu atenție
2. **Google-uiți** eroarea (foarte util!)
3. **Consultați Cursul 1** pentru sintaxă
4. **Întrebați** profesorul sau colegii
5. **Apoi** consultați soluțiile

### 5. "Trebuie să scriu exact ca în soluții?"
**NU!** Dacă funcționează și e corect, e perfect! Există multe moduri de a rezolva.

### 6. "Ce înseamnă 'in-place'?"
Modificarea unei structuri de date fără a crea una nouă:
```python
# In-place - modifică original
lista = [1, 2, 3]
lista.append(4)
print(lista)  # [1, 2, 3, 4]

# Nou obiect - lasă originalul intact
lista = [1, 2, 3]
lista_noua = lista + [4]
print(lista)      # [1, 2, 3]
print(lista_noua) # [1, 2, 3, 4]
```

### 7. "Cum verific dacă funcția mea e corectă?"
```python
# Testați cu cazuri simple
def suma_lista(lista):
    # ... codul vostru

# Test manual
rezultat = suma_lista([1, 2, 3])
print(f"Rezultat: {rezultat}, Așteptat: 6")

# Test cu date din homework
populatie_totala = calculeaza_populatie_totala(date_regiuni)
print(f"Total: {populatie_totala:,} locuitori")
```

---

## 🎁 Resurse Suplimentare

### Documentație Python:
- [Python String Methods](https://docs.python.org/3/library/stdtypes.html#string-methods)
- [Python Lists](https://docs.python.org/3/tutorial/datastructures.html#more-on-lists)
- [Python Dictionaries](https://docs.python.org/3/tutorial/datastructures.html#dictionaries)

### Tutoriale:
- [Real Python - Working with Lists](https://realpython.com/python-lists-tuples/)
- [Real Python - Python Dictionaries](https://realpython.com/python-dicts/)

### Exerciții Extra:
- [Exercism Python Track](https://exercism.org/tracks/python)
- [Python Principles](https://pythonprinciples.com/)

---

## 📧 Contact și Suport

### Pentru Studenți:
- 📧 Email profesor: [email profesorului]
- 💬 Forum curs: [link dacă există]
- 👥 Grup studenți: [link dacă există]

### Pentru Feedback:
Dacă găsiți erori sau aveți sugestii de îmbunătățire:
- Raportați profesorului
- Propuneți îmbunătățiri
- Împărtășiți soluții creative

---

## 📜 Licență și Utilizare

Aceste materiale sunt create pentru **Cursul Python - Centrul Național de Statistică**.

**Permis:**
- ✅ Utilizare educațională
- ✅ Modificare pentru nevoile cursului
- ✅ Distribuire către studenți

**Nepermis:**
- ❌ Utilizare comercială fără permisiune
- ❌ Revendicare ca lucrare proprie

---

## 🌟 Succes la Lucru!

Amintiți-vă:
- 🎯 **Practicat** > Lectură pasivă
- 🔄 **Repetiție** > Perfectiune imediată
- 🤔 **Înțelegere** > Memorare
- 🚀 **Progres** > Perfectiune

**Happy Coding! 🐍💻📊**

---

*Ultima actualizare: Noiembrie 2025*
*Versiune: 1.0*
