

# Chapitre 5 : Les chaînes de caractères 🔡

## Introduction

- Un **caractère** est un symbole : lettre, chiffre, ponctuation, etc.
- Une **chaîne de caractères** (ou *string*) est une **suite** de caractères 📜.
- Une chaîne **vide** est une chaîne sans caractère.

---

## Chaînes de caractères en Python 🐍

- Type **str**.
- **Immuables** ➔ On ne peut pas les modifier après création.

### Déclaration

```python
chaine1 = 'Bonjour'
chaine2 = "Bonjour"
```

### Chaîne multilignes

```python
chaine_multi = """Ceci est
une chaîne
multiligne"""
```

---

## Indexation et Longueur 🔢

- Chaque caractère a un **indice** (positif ou négatif).

### Accès :

```python
chaine[0]   # Premier caractère
chaine[-1]  # Dernier caractère
```

### Longueur :

```python
len(chaine)
```

---

## Parcourir une chaîne 🔄

### Avec indices

```python
for i in range(len(chaine)):
    print(chaine[i])
```

### Sans indices

```python
for caractere in chaine:
    print(caractere)
```

### Avec enumerate

```python
for i, caractere in enumerate(chaine):
    print(i, caractere)
```

---

## Opérations sur les chaînes ✨

- **Concaténation** :

```python
chaine = "Hello" + " " + "World"
```

- **Appartenance** :

```python
"e" in "Hello"  # True
```

- **Comparaison** :

```python
"a" < "b"  # True
```

---

## Slicing (Tranches) 🔪

```python
chaine[start:end:step]
```
- `start` : où commencer
- `end` : où s'arrêter (exclu)
- `step` : pas

Exemple :

```python
chaine = "Bonjour"
print(chaine[1:5:2])  # "oo"
```

---

## Méthodes courantes 🛠️

| Méthode | Description |
|:--|:--|
| `chaine.upper()` | Majuscules |
| `chaine.lower()` | Minuscules |
| `chaine.capitalize()` | Première lettre en majuscule |
| `chaine.strip()` | Enlève les espaces |
| `chaine.replace(a, b)` | Remplace `a` par `b` |
| `chaine.split(sep)` | Découpe la chaîne |
| `'séparateur'.join(liste)` | Concatène avec un séparateur |

---

## Recherche et Vérification 🔍

- `chaine.find(sub)` ➔ Indice de `sub` ou `-1`.
- `chaine.index(sub)` ➔ Comme `find()`, mais erreur si absent.
- `chaine.count(sub)` ➔ Nombre d'occurrences de `sub`.

### Vérifications :

- `isalpha()` : alphabetique ?
- `isdigit()` : chiffres uniquement ?
- `isalnum()` : alpha-numérique ?
- `isspace()` : uniquement des espaces ?

---

## Exemples pratiques 🎯

### Inverser une chaîne

```python
chaine[::-1]
```

### Compter les mots

```python
len(chaine.split())
```

### Remplacer un mot

```python
chaine.replace('ancien', 'nouveau')
```

---

# Solutions des Exercices 🧠

## Exercice 1

> Que vaut chaque instruction ?

Solutions :
1. `print(a[0])` ➔ `B`
2. `print(a[3])` ➔ `j`
3. `print(a[-3])` ➔ `o`
4. `print(len(a))` ➔ `7`
5. `print(a[-8:-3])` ➔ **Erreur** (indice hors limite)
6. `print(a[0:4])` ➔ `Bonj`
7. `print(a[1:5:2])` ➔ `oj`
8. `print(a[0]+a[-1])` ➔ `Br`
9. `print(a[0]+4*a[-1])` ➔ `Brrrr`
10. `print('B' in a)` ➔ `True`
11. `print('b' in a)` ➔ `False`
12. `print(a[1]=='o')` ➔ `True`
13. `print(a[1]='B')` ➔ **Erreur** (affectation impossible)

---

## Exercice 2

> Nombre de voyelles dans une phrase.

```python
phrase = input("Entrez une phrase : ")
voyelles = "aeiouyAEIOUY"
compte = 0
for c in phrase:
    if c in voyelles:
        compte += 1
print("Nombre de voyelles :", compte)
```

---

## Exercice 3

> Compter le nombre de lettres d’un mot.

```python
mot = input("Entrez un mot : ")
print("Nombre de lettres :", len(mot))
```

---

## Exercice 4

> Compter les lettres `e` dans une phrase.

```python
phrase = input("Entrez une phrase : ")
print("Nombre de 'e' :", phrase.count('e'))
```

---

## Exercice 5

> Afficher un mot à l'envers.

```python
mot = input("Entrez un mot : ")
print("Mot inversé :", mot[::-1])
```

---

## Exercice 6

> Afficher un prénom avec `*` entre chaque lettre.

```python
prenom = input("Entrez votre prénom : ")
print('*'.join(prenom))
```

---




