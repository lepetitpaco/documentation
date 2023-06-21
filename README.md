# Sommaire

- [Sommaire](#sommaire)
  - [I. Comment faire du Markdown](#i-comment-faire-du-markdown)
    - [A. Titres](#a-titres)
    - [B. Listes](#b-listes)
      - [Formatter le texte](#formatter-le-texte)
      - [Listes à puces](#listes-à-puces)
      - [Listes à numéros](#listes-à-numéros)
      - [Liste à taches](#liste-à-taches)
      - [Listes imbriquées](#listes-imbriquées)
    - [C. Liens et images](#c-liens-et-images)
      - [Image sans taille spécifiée](#image-sans-taille-spécifiée)
      - [Image avec taille spécifiée](#image-avec-taille-spécifiée)
      - [Lien sans texte](#lien-sans-texte)
      - [Lien avec texte](#lien-avec-texte)
    - [D. Blocs de code](#d-blocs-de-code)
      - [Code en ligne](#code-en-ligne)
      - [Code multiligne](#code-multiligne)
      - [Coloration syntaxique](#coloration-syntaxique)
  - [II. Plugins VSCODE](#ii-plugins-vscode)

## I. Comment faire du Markdown

### A. Titres

```markdown
# Titre de niveau 1
## Titre de niveau 2
### Titre de niveau 3
#### Titre de niveau 4
##### Titre de niveau 5
###### Titre de niveau 6
```

### B. Listes

#### Formatter le texte

```markdown
**Gras**
*italique*
***italique gras***
~~Barré~~
```

**Gras**

*italique*

***italique gras***

~~Barré~~

#### Listes à puces

```markdown
- Élément 1
- Élément 2
- Élément 3
```

- Élément 1
- Élément 2
- Élément 3

#### Listes à numéros

```markdown
1. Élément 1
2. Élément 2
3. Élément 3
```

1. Élément 1
2. Élément 2
3. Élément 3

La numérotation est gérée autimatiquement par markdown (appuie sur entrée pour aller à la ligne)

#### Liste à taches

```markdown
- [ ] Tâche 1
- [x] Tâche 2
- [ ] Tâche 3
```

- [ ] Tâche 1
- [x] Tâche 2
- [ ] Tâche 3

Une nouvelle puce avec case à cocher est générée en allant à la ligne.

#### Listes imbriquées

```markdown
1. Premier niveau
   - Deuxième niveau, élément 1
   - Deuxième niveau, élément 2
      1. Troisième niveau, élément 1
      2. Troisième niveau, élément 2
   - Deuxième niveau, élément 3
2. Premier niveau, élément 2
```

1. Premier niveau
   - Deuxième niveau, élément 1
   - Deuxième niveau, élément 2
      1. Troisième niveau, élément 1
      2. Troisième niveau, élément 2
   - Deuxième niveau, élément 3
2. Premier niveau, élément 2

### C. Liens et images

#### Image sans taille spécifiée

```markdown
![Texte alternatif](chemin/vers/image.jpg)
```

#### Image avec taille spécifiée

```markdown
<img src="chemin/vers/image.jpg" alt="Texte alternatif" width="300" height="200">
```

#### Lien sans texte

```markdown
<URL_du_lien>
```

#### Lien avec texte

```markdown
[Texte du lien](URL_du_lien)
```

### D. Blocs de code

#### Code en ligne

```markdown
Voici un extrait de code en ligne :`print("Bonjour, monde!")`.
```

Voici un extrait de code en ligne : `print("Bonjour, monde!")`.

#### Code multiligne

```markdown
    ```
    function addition(a, b) {
    return a + b;
    }

    console.log(addition(2, 3));
    ```
```

```
function addition(a, b) {
return a + b;
}

console.log(addition(2, 3));
```

#### Coloration syntaxique

```
    ```python
    def multiplication(a, b):
    return a * b

    print(multiplication(2, 3))
    ```
```

```python
def multiplication(a, b):
return a * b

print(multiplication(2, 3))
```

**Penser à utiliser les raccourcis avec vs code pour générer les différents éléments
Mots clés :**

- list
- code

## II. Plugins VSCODE

- [Markdown Preview Enhanced](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced)
  - Permet de visualiser son markdown en direct
  
- [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)
  - Formatte le markdown
