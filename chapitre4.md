
```python
"""*
# Chapitre 4 : Structures de Contrôles 🚀

## Introduction 🔄
Les programmes s'exécutent normalement de manière séquentielle.  
Parfois, il faut choisir entre plusieurs chemins ou répéter des instructions.

Deux grands types :
- **Structures conditionnelles** 📈
- **Structures répétitives** 🔄

---

## Structures de contrôle conditionnelles ✅

### 1. `if` (simple)
Exécute un bloc seulement si la condition est vraie.

```python
if condition:
    instructions
```

---

### 2. `if...else` (double)
Choisit entre deux blocs selon la condition.

```python
if condition:
    instructions si vrai
else:
    instructions si faux
```

---

### 3. `if...elif...else` (multiple)
Plusieurs tests en chaîne.

```python
if condition1:
    instructions1
elif condition2:
    instructions2
else:
    instructions par défaut
```

---

## Structures de contrôle répétitives ⟳

### 1. `while`
Répète tant que la condition est vraie.

```python
while condition:
    instructions
```

---

### 2. `for`
Répète pour un nombre connu d'étapes.

```python
for i in range(debut, fin, pas):
    instructions
```

*Remarque :* `range(debut, fin, pas)` génère une séquence de nombres.

---

### 3. Boucles infinies avec `while` et `for` ♻️

**Boucle while infinie (classique) :**
```python
while True:
    print("Cette boucle ne s'arrête jamais 🔀")
```
Utilisée pour écouter un événement ou répéter sans fin jusqu'à un `break`.

**Boucle for infinie (moins naturel) :**
```python
import itertools

for _ in itertools.cycle([0]):
    print("Boucle infinie avec for 🛠️")
```

---

### Instructions utiles dans les boucles :

- `break` 🛉 : Sort de la boucle prématurément.
- `continue` ➡️ : Passe directement à l'itération suivante.
- `else` : S'exécute si la boucle n'est **pas** interrompue par un `break`.

---

# Solutions des Exercices 🔮

---

## Exercice 1
Demander un nombre et dire s'il est positif, négatif ou nul.

```python
n = int(input("Entrez un nombre : "))
if n > 0:
    print("Positif 💚")
elif n < 0:
    print("Négatif 💙")
else:
    print("Nul 💜")
```

---

## Exercice 2
Produit de deux nombres : positif ou négatif ?

```python
a = int(input("Premier nombre : "))
b = int(input("Deuxième nombre : "))
produit = a * b
if produit > 0:
    print("Produit positif 💚")
elif produit < 0:
    print("Produit négatif 💙")
else:
    print("Produit nul 💜")
```

---

## Exercice 3
Table de multiplication.

```python
n = int(input("Entrez un nombre : "))
for i in range(1, 10):
    print(f"{n} x {i} = {n*i}")
```

---

## Exercice 4
Somme jusqu'à un nombre donné.

```python
n = int(input("Entrez un nombre : "))
somme = 0
for i in range(1, n+1):
    somme += i
print("Somme =", somme)
```

---

## Exercice 5
Demander un nombre entre 1 et 3 jusqu'à ce qu'il soit correct.

```python
while True:
    n = int(input("Entrez un nombre entre 1 et 3 : "))
    if 1 <= n <= 3:
        print("Bravo 👍")
        break
    else:
        print("Essayez encore !")
```

---

## Exercice 6
Trouver le plus grand parmi 20 nombres.

```python
maxi = None
pos = 0
for i in range(1, 21):
    n = int(input(f"Entrez le nombre numéro {i} : "))
    if (maxi is None) or (n > maxi):
        maxi = n
        pos = i
print(f"Le plus grand est {maxi} (position {pos})")
```

---

## Exercice 7
Trouver le plus grand sans savoir combien de nombres seront entrés (arrêt sur 0).

```python
maxi = None
pos = 0
compteur = 0
while True:
    n = int(input("Entrez un nombre (0 pour finir) : "))
    if n == 0:
        break
    compteur += 1
    if (maxi is None) or (n > maxi):
        maxi = n
        pos = compteur
print(f"Le plus grand est {maxi} (position {pos})")
```

---

## Exercice 8
Afficher un triangle d'étoiles.

```python
n = int(input("Entrez la taille du triangle : "))
for i in range(n):
    print(' '*(n-i-1) + '*'*(2*i+1))
```

---

## Exercice 9
Vérifier si les chiffres d'un nombre sont distincts.

```python
n = input("Entrez un entier : ")
if len(n) == len(set(n)):
    print("Cet entier est distinct 🌟")
else:
    print("Cet entier n'est pas distinct 💥")
```

---


*"""
```

---


---

Veux-tu aussi que je te prépare directement un fichier `.py` ou `.md` pour que tu n’aies qu’à faire un drag-and-drop ? 🚀  
(Dis-moi si tu veux 😎)
