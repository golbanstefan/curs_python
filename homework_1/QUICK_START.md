# 🚀 Ghid Rapid de Start - Temă 1 (Curs 1)

## ⚡ Înc epi Rapid (5 minute)

### 1. Ce Este Această Temă?
Veți analiza date statistice despre 10 regiuni moldovenești folosind **doar Python de bază** (fără biblioteci externe).

**Veți învăța:**
- Curățarea datelor "murdare"
- Calcularea statisticilor
- Gruparea și filtrarea
- Crearea de funcții reutilizabile

### 2. Ce Fișiere Folosesc?

| Fișier | Când să-l folosiți |
|--------|-------------------|
| **`homework_1_statistics_practice.ipynb`** | 📝 **AICI lucrați!** Exercițiile voastre |
| **`homework_1_hints.ipynb`** | 💡 Când aveți nevoie de structură/hint-uri |
| **`homework_1_solutions.ipynb`** | ✅ Pentru verificare (după ce ați încercat!) |
| **`README.md`** | 📚 Documentație completă, detalii |
| **`QUICK_START.md`** | ⚡ Acest fișier - start rapid |

### 3. Cum Încep?

```bash
# 1. Navigați în folder
cd homework_1/

# 2. Porniți Jupyter
jupyter notebook

# 3. Deschideți homework_1_statistics_practice.ipynb
```

---

## 📋 Workflow Recomandat

### Pentru Începători:
```
1. Citiți cerința exercițiului
2. Deschideți homework_1_hints.ipynb pentru structură
3. Scrieți codul în homework_1_statistics_practice.ipynb
4. Testați funcția
5. Dacă e corect → următorul exercițiu
6. Dacă nu funcționează → debug, apoi consultați soluțiile
```

### Pentru Experimentați:
```
1. Citiți cerința
2. Scrieți direct în homework_1_statistics_practice.ipynb
3. Testați
4. Consultați soluțiile doar pentru comparație
```

---

## 🎯 Exerciții - Pe Scurt

### 🧹 Parte 1: Curățare (Ex. 1-4)
Curățați date cu probleme:
- Spații extra: `"  Cahul"` → `"Cahul"`
- Majuscule: `"AGRICULTURĂ"` → `"Agricultură"`
- Valori lipsă: `None` → calculați media și completați

**Dificultate:** ⭐⭐ Mediu
**Timp estimat:** 1-2 ore

### 📊 Parte 2: Analiză (Ex. 5-15)
Analizați datele curate:
- Afișare, extragere, calculare statistici
- Filtrare, grupare, clasificare
- Găsire extreme, sortare, comparație

**Dificultate:** ⭐⭐⭐ Mediu-Avansat
**Timp estimat:** 4-6 ore

### 🎁 Bonus: Dashboard (Ex. 16)
Combinați toate funcțiile într-un raport complet

**Dificultate:** ⭐⭐⭐⭐⭐ Avansat
**Timp estimat:** 1-2 ore

---

## 💡 Top 5 Sfaturi

### 1. **Testați Incremental**
```python
# ❌ NU faceți așa:
def functie_mare():
    # 50 linii de cod deodată
    pass

# ✅ Faceți așa:
def functie_mare():
    # Scrieți 5 linii
    print("DEBUG: Am ajuns aici")  # Testați
    # Scrieți încă 5 linii
    print("DEBUG: Am ajuns și aici")  # Testați
```

### 2. **Citiți Erorile**
```python
# Eroare:
# KeyError: 'populatie'

# Înseamnă: cheia nu există în dicționar
# Verificați: print(regiune.keys())
```

### 3. **Folosiți print() pentru Debug**
```python
def calculeaza_ceva(lista):
    suma = 0
    print(f"DEBUG: Lista are {len(lista)} elemente")
    for element in lista:
        suma += element
        print(f"DEBUG: suma acum = {suma}")
    return suma
```

### 4. **Nu Vă Grăbiți la Soluții**
- ⏱️ Încercați minim **30 de minute** per exercițiu dificil
- 🤔 Gândiți-vă la mai multe abordări
- 📝 Schițați logica pe hârtie înainte

### 5. **Verificați Tipurile de Date**
```python
# Dacă ceva nu funcționează:
valoare = regiune["populatie"]
print(f"Valoare: {valoare}, Tip: {type(valoare)}")

# Verificați None:
if valoare is None:
    print("Este None!")
```

---

## 🔧 Comenzi Utile Jupyter

```python
# Rulare celulă: Shift + Enter
# Autocompletare: Tab
# Help funcție: Shift + Tab (cu cursorul pe funcție)

# Afișare variabile:
print(date_regiuni[0])  # Primul dicționar

# Tipuri de date:
print(type(date_regiuni))  # <class 'list'>

# Lungimi:
print(len(date_regiuni))  # 10

# Chei dicționar:
print(date_regiuni[0].keys())
```

---

## 📊 Datele - Rapid

```python
# 10 regiuni:
Chișinău, Bălți, Cahul, Ungheni, Soroca,
Orhei, Edineț, Comrat, Strășeni, Hîncești

# 8 câmpuri per regiune:
- regiune (str): numele
- populatie (int): număr locuitori
- rata_ocupare (float): % ocupare
- venit_mediu (float): venit în lei
- rata_alfabetizare (float): % alfabetizare
- sector_dominant (str): Agricultură/Industrie/Servicii
- numar_intreprinderi (int): număr întreprinderi
- rata_somaj (float): % șomaj

# Date "murdare" (intenționate):
- Spații: "Chișinău ", "  Cahul"
- Majuscule: "servicii", "AGRICULTURĂ"
- None: în rata_ocupare, venit_mediu, etc.
```

---

## ❓ Întrebări Frecvente

### "Cât timp durează?"
**4-10 ore** total, în funcție de experiență.

### "Trebuie să rezolv toate?"
**Minimum:** Exercițiile 1-12 pentru notă de trecere
**Recomandat:** Toate (1-15) pentru învățare completă
**Bonus:** Exercițiul 16 pentru provocare

### "Pot folosi pandas?"
**NU!** Doar Python standard library. Pandas vine în cursul următor.

### "Când consult soluțiile?"
După **minim 30 min** de încercare serioasă per exercițiu dificil.

### "Ce fac dacă sunt blocat?"
1. Citește din nou cerința
2. Verifică sintaxa în Cursul 1
3. Folosește homework_1_hints.ipynb
4. Google eroarea
5. Întreabă profesorul/colegii
6. **Apoi** consultă soluțiile

### "Trebuie să scriu exact ca în soluții?"
**NU!** Există multe moduri corecte. Dacă funcționează și e logic, e perfect!

---

## 🎯 Checklist Înainte de a Începe

- ☐ Am instalat Python 3.7+ și Jupyter
- ☐ Am descărcat toate fișierele din homework_1/
- ☐ Am citit acest ghid rapid
- ☐ Am deschis homework_1_statistics_practice.ipynb
- ☐ Am o foaie de hârtie pentru schițe (opțional dar util!)
- ☐ Am alocat timp suficient (nu vă grăbiți!)

---

## 🆘 Când Ceva Nu Merge

### Python nu pornește:
```bash
# Încercați:
python3 --version
# sau
python --version

# Trebuie să vedeți: Python 3.x.x
```

### Jupyter nu pornește:
```bash
# Instalați:
pip install jupyter
# sau
pip3 install jupyter

# Porniți:
jupyter notebook
```

### Erori în cod:
1. **Citiți mesajul** de eroare cu atenție
2. **Căutați pe Google** eroarea exactă
3. **Verificați sintaxa** - lipsesc două puncte `:` ?
4. **Verificați indentarea** - e corectă?
5. **Print debug** - adăugați print() peste tot

---

## 📚 Resurse Rapide

### Sintaxă Python:
- **Liste:** `lista.append(x)`, `lista[0]`, `for x in lista:`
- **Dicționare:** `dict["key"]`, `dict.keys()`, `dict.items()`
- **String:** `.strip()`, `.title()`, `.lower()`, `.upper()`
- **Funcții:** `def nume(parametri): ... return rezultat`
- **Condiții:** `if x > 5: ... elif x > 3: ... else: ...`
- **Bucle:** `for i in range(10): ...`, `while x < 10: ...`

### Verificare None:
```python
if valoare is None:
    # tratează None
else:
    # folosește valoarea
```

### Formatare numere:
```python
print(f"{numar:,}")      # 532513 → 532,513
print(f"{numar:.2f}")    # 67.5 → 67.50
print(f"{numar:>10}")    # aliniere dreapta
```

---

## 🎉 Gata de Început!

**Următorii pași:**
1. ✅ Deschideți `homework_1_statistics_practice.ipynb`
2. ✅ Citiți Exercițiul 1
3. ✅ Începeți să codați!

**Amintiți-vă:**
- 🎯 Practicați > Lectura pasivă
- 🔄 Progres > Perfecțiune
- 🤔 Înțelegere > Memorare

---

**Mult Succes! 🚀 Happy Coding! 🐍**

*Pentru detalii complete → README.md*
*Pentru structură/hint-uri → homework_1_hints.ipynb*
*Pentru soluții → homework_1_solutions.ipynb (după încercare!)*
