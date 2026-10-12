# Tableau 

Pour créer un tableau en HTML, utilisez les balises `<table>`, `<tr>`, `<td>` et `<th>` pour structurer vos données en lignes et en colonnes.

## Structure de base d’un tableau HTML

1. **Balise `<table>`** : C'est le conteneur principal du tableau. Elle englobe toutes les autres balises.

2. **Balise `<tr>`** : Utilisée pour créer une ligne dans le tableau.

3. **Balise `<td>`** : Représente une cellule de données dans une ligne.

4. **Balise `<th>`** : Utilisée pour créer une cellule d'en-tête. Son texte est généralement affiché en gras et centré.

## Fusionner des cellules

### 1. Attribut `colspan`

L'attribut `colspan` permet de fusionner plusieurs colonnes horizontalement.

Exemple : `colspan="3"` permet à une cellule d'occuper trois colonnes.

### 2. Attribut `rowspan`

L'attribut `rowspan` permet de fusionner plusieurs lignes verticalement.

Exemple : `rowspan="2"` permet à une cellule d'occuper deux lignes.

## Exemple HTML

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tableau HTML</title>
</head>
<body>

    <table border="1">
        <tr>
            <th colspan="3">En-tête sur 3 colonnes</th>
        </tr>

        <tr>
            <td rowspan="2">Cellule fusionnée sur 2 lignes</td>
            <td>Colonne 2, ligne 1</td>
            <td>Colonne 3, ligne 1</td>
        </tr>

        <tr>
            <td colspan="2">Cellule fusionnée sur 2 colonnes</td>
        </tr>

        <tr>
            <td>Colonne 1, ligne 3</td>
            <td>Colonne 2, ligne 3</td>
            <td>Colonne 3, ligne 3</td>
        </tr>
    </table>

</body>
</html>
```

## Résultat

| Cellule fusionnée sur 2 lignes | Colonne 2, ligne 1 | Colonne 3, ligne 1 |
|---|---|---|
|  | Cellule fusionnée sur 2 colonnes | |
| Colonne 1, ligne 3 | Colonne 2, ligne 3 | Colonne 3, ligne 3 |