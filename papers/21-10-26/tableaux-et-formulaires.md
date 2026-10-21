# 7. Les tableaux

Un tableau sert à présenter des **données** en lignes et en colonnes (jamais à mettre en page un site).

```html
<table border="1">
  <caption>Notes du premier trimestre</caption>
  <thead>
    <tr>
      <th>Élève</th>
      <th>Maths</th>
      <th>Français</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Amine</td>
      <td>15</td>
      <td>12</td>
    </tr>
    <tr>
      <td>Sarra</td>
      <td>17</td>
      <td>14</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>Moyenne</td>
      <td>16</td>
      <td>13</td>
    </tr>
  </tfoot>
</table>
```

## Fusionner des cellules : colspan et rowspan

```html
<table border="1">
  <tr>
    <th colspan="2">Horaires</th>   <!-- fusion de 2 colonnes -->
  </tr>
  <tr>
    <td rowspan="2">Lundi</td>      <!-- fusion de 2 lignes -->
    <td>Matin : 8h - 12h</td>
  </tr>
  <tr>
    <td>Après-midi : 14h - 18h</td>
  </tr>
</table>
```

| Balise | Rôle |
|---|---|
| `<table>` | Conteneur du tableau. |
| `<caption>` | Titre du tableau (juste après `<table>`). |
| `<thead>` | Groupe de l'en-tête du tableau. |
| `<tbody>` | Groupe du corps du tableau. |
| `<tfoot>` | Groupe du pied de tableau (totaux...). |
| `<tr>` | Ligne (table row). |
| `<th>` | Cellule d'en-tête (gras et centrée par défaut). Attribut `scope="col"` ou `"row"`. |

---

# Les formulaires

## Les types de champ `<input>`

> Cette partie de la photo est floue : les types et leurs descriptions ont été reconstitués au mieux. À vérifier avec ton cours.

| Valeur de `type` | Utilisation |
|---|---|
| `text` | Texte sur une ligne. |
| `email` / `url` / `tel` | Adresse e-mail, URL, téléphone (validation et clavier adaptés). |
| `password` | Mot de passe (caractères masqués). |
| `number` / `range` | Nombre avec min, max, step / curseur. |
| `date` / `time` / `datetime-local` | Sélecteur de date, d'heure, de date et heure. |
| `color` | Sélecteur de couleur. |
| `search` | Champ de recherche. |
| `radio` | Bouton radio : un seul choix parmi plusieurs (même `name`). |
| `checkbox` | Case à cocher : plusieurs choix possibles. |
| `file` | Envoi de fichier (`accept` limite les types). |
| `hidden` | Champ caché, envoyé avec le formulaire. |
| `submit` / `reset` / `button` | Envoyer, réinitialiser, bouton générique. |

## Les autres balises de formulaire

| Balise | Rôle |
|---|---|
| `<form>` | Conteneur du formulaire (`action`, `method`). |
| `<label>` | Étiquette d'un champ ; `for` doit égaler l'`id` du champ (clic et accessibilité). |
| `<input>` | Champ de saisie, selon son attribut `type`. |
| `<textarea>` | Zone de texte sur plusieurs lignes (`rows`, `cols`). |
| `<select>` | Liste déroulante. |
| `<option>` | Choix d'une liste. `value` = valeur envoyée, `selected` = présélection. |
| `<optgroup>` | Regroupe des `<option>` sous une étiquette (`label`). |
| `<datalist>` | Suggestions de saisie, reliées à un `input` par l'attribut `list`. |
| `<button>` | Bouton (type `submit`, `reset` ou `button`). |
| `<fieldset>` | Regroupe des champs liés. |
| `<legend>` | Titre d'un `<fieldset>`. |
| `<output>` | Affiche le résultat d'un calcul. |

## Attributs de validation courants

| Attribut | Effet |
|---|---|
| `required` | Champ obligatoire. |
| `placeholder` | Texte d'aide grisé dans le champ vide. |
| `name` | Nom de la donnée envoyée au serveur (indispensable). |
