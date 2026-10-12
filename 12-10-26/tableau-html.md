# Tableau HTML

Pour créer un tableau en HTML, utilisez les balises `<table>`, `<tr>`, `<td>` et `<th>` pour structurer vos données en lignes et colonnes.

## Structure de base d’un tableau HTML

1. **Balise `<table>`**  
   C’est le conteneur principal de votre tableau. Elle englobe toutes les autres balises du tableau.

2. **Balise `<tr>`**  
   Utilisée pour créer une nouvelle ligne dans le tableau. Chaque ligne doit être entourée de balises `<tr>`.

3. **Balise `<td>`**  
   Représente une cellule de données dans une ligne. Chaque cellule doit être placée à l’intérieur d’une balise `<tr>`.

4. **Balise `<th>`**  
   Utilisée pour créer des en-têtes de colonnes ou de lignes. Le texte dans une cellule `<th>` est généralement affiché en gras et centré.

## Exemple de tableau HTML

```html
<table>
  <tr>
    <th>Nom</th>
    <th>Âge</th>
    <th>Ville</th>
  </tr>
  <tr>
    <td>Amine</td>
    <td>20</td>
    <td>Gafsa</td>
  </tr>
  <tr>
    <td>Sara</td>
    <td>22</td>
    <td>Tunis</td>
  </tr>
</table>
```

## Activité

Créez un tableau HTML contenant trois colonnes : **Nom**, **Âge** et **Ville**. Ajoutez au moins deux lignes de données.
