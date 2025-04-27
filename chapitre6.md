

# Chapitre 6 : Fonctions et Modules 🛠️

---

## Introduction

- Une **fonction** est un sous-programme qui réalise une tâche spécifique.
- Elle **évite les répétitions**, rend le code **plus clair** et **réutilisable**.
- Deux types :
  - **Fonctions prédéfinies** 🏗️ (ex: `print()`, `input()`, `len()`, etc.)
  - **Fonctions définies par l'utilisateur** 🧑‍💻

---

## Fonctions intégrées en Python 🐍

Quelques fonctions prédéfinies utiles :

| Fonction | Rôle |
|:--|:--|
| `input()` | Lire une entrée utilisateur |
| `int()` | Convertir en entier |
| `print()` | Afficher une sortie |
| `len()` | Longueur d'un objet |
| `list()` | Créer une liste |
| `max()` | Plus grand élément |
| `min()` | Plus petit élément |
| `range()` | Générer une séquence |
| `set()` | Créer un ensemble |
| `str()` | Convertir en chaîne |
| `type()` | Obtenir le type d'un objet |

---

## Fonctions définies par l'utilisateur 👨‍💻

### Syntaxe pour définir une fonction :

```python
def nom_de_fonction(param1, param2, ...):
    # Corps de la fonction
    return valeur
```

- **`def`** ➔ mot-clé pour définir une fonction.
- **`return`** ➔ renvoyer une valeur (facultatif).

---

## Valeur retournée par une fonction 🎯

- Utiliser `return` pour **envoyer un résultat**.
- Sans `return`, Python retourne **None** par défaut.
- ⚡ Attention : `print()` ≠ `return`.

---

## Appeler une fonction 📞

Pour exécuter une fonction :

```python
nom_de_fonction(arguments)
```

---

## Exemples de fonctions

### Fonction sans paramètres et sans retour :

```python
def bonjour():
    print("Bonjour !")

bonjour()
```

---

### Fonction avec paramètres et retour de valeur :

```python
def minimum(a, b):
    return min(a, b)

print("Le plus petit nombre est :", minimum(26, 54))
```

---

### Fonction avec paramètres sans retour :

```python
def afficher_min(a, b):
    print("Le plus petit nombre est :", min(a, b))

afficher_min(23, 15)
```

---

### Fonction sans paramètres mais avec retour :

```python
def generer_nombre():
    return 19.7192

print(generer_nombre())
```

---

## Arguments positionnels et arguments par mot-clé 📚

### Arguments positionnels

- Ordre **obligatoire** lors de l'appel.

```python
def soustraction(a, b):
    return a - b

print("a - b =", soustraction(20, 6))  # 14
print("a - b =", soustraction(6, 20))  # -14
```

---

### Arguments par mot-clé

- Passage par **nom de paramètre**, ordre **libre**.

```python
def afficher(a=10, b=20):
    print("a =", a, "b =", b)

afficher(b=5, a=7)
```

⚡ **Attention** : Les arguments positionnels doivent être **avant** les arguments par mot-clé.

---

## Variables locales et globales 🌍

| Type | Description |
|:--|:--|
| Locale | Définie **dans une fonction**, visible **seulement** dedans |
| Globale | Définie **hors fonction**, visible **partout** |

### Utiliser le mot-clé `global` :

```python
x = 10

def modifier():
    global x
    x = 20

modifier()
print(x)  # 20
```

---

## Les Modules 📦

- **Module** = Fichier `.py` contenant des **fonctions, classes, variables**.
- Exemple : `salutations.py`

```python
def dire_bonjour():
    print("Bonjour !")

def dire_bonsoir():
    print("Bonsoir !")
```

---

### Importer un module :

```python
import salutations

salutations.dire_bonjour()
salutations.dire_bonsoir()
```

---

### Importer une fonction spécifique :

```python
from salutations import dire_bonjour

dire_bonjour()
```

---

## Obtenir de l'aide 🆘

Pour explorer les modules :

```python
import math
dir(math)  # Liste les fonctions du module
help(math.sqrt)  # Aide sur la fonction sqrt()
help('modules')  # Voir tous les modules installés
```

---

# Exercices 🧠

## Exercice 1

> Définir et appeler une fonction `Bonjour` qui affiche "Bonjour !".

```python
def Bonjour():
    print("Bonjour !")

Bonjour()
```

---

## Exercice 2

> Définir une fonction `Somme(a, b)` qui retourne la somme de deux nombres.

```python
def Somme(a, b):
    return a + b

print(Somme(5, 7))  # 12
```

---

## Exercice 3

> Définir une fonction `Positif(n)` qui retourne `True` si un nombre est positif, sinon `False`.

```python
def Positif(n):
    return n > 0

print(Positif(5))   # True
print(Positif(-3))  # False
```

---

## Exercice 4

> Créer une fonction qui vérifie si un nombre est **premier**.

```python
def est_premier(n):
    if n <= 1:
        return False
    for i in range(2, int(n**0.5)+1):
        if n % i == 0:
            return False
    return True

print(est_premier(7))   # True
print(est_premier(9))   # False
```

---

