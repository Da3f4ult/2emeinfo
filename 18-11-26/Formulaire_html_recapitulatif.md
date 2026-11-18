# Récapitulatif des éléments d'un formulaire HTML

Chaque élément est présenté avec son rôle et un exemple de code.

---

## 1. La structure de base

Un formulaire permet à l'utilisateur de saisir des informations et de les envoyer au serveur. Il est créé avec la balise `<form>`.

```html
<form action="traitement.php" method="post">
  éléments du formulaire ...
</form>
```

**Attributs importants :**

- `action` indique la page qui reçoit les données.
- `method` précise la méthode d'envoi (souvent `get` ou `post`).

---

## 2. Les champs de saisie (balise `<input>`)

| Élément | Rôle | Exemple de code |
|---------|------|-----------------|
| **Texte** | Saisir un texte court : nom, prénom. | `<input type="text" name="nom" placeholder="Votre nom">` |
| **Mot de passe** | Saisir un mot de passe ; les caractères sont masqués. | `<input type="password" name="mdp">` |
| **E-mail** | Saisir une adresse e-mail. Le navigateur peut vérifier son format. | `<input type="email" name="email">` |
| **Nombre** | Saisir une valeur numérique. On peut ajouter `min`, `max` et `step`. | `<input type="number" name="age" min="1" max="100">` |
| **Téléphone** | Saisir un numéro de téléphone. | `<input type="tel" name="telephone">` |
| **Adresse web** | Saisir une adresse internet. | `<input type="url" name="site">` |
| **Recherche** | Champ destiné à une recherche. | `<input type="search" name="recherche">` |
| **Date** | Choisir une date dans un calendrier. | `<input type="date" name="date_naissance">` |
| **Heure** | Choisir une heure. | `<input type="time" name="heure">` |
| **Fichier** | Sélectionner un fichier sur l'appareil. | `<input type="file" name="document">` |
| **Couleur** | Choisir une couleur. | `<input type="color" name="couleur">` |
| **Curseur** | Choisir une valeur à l'aide d'un curseur. | `<input type="range" name="niveau" min="0" max="10">` |
| **Case à cocher** | Cocher zéro, une ou plusieurs options. | `<input type="checkbox" name="interets" value="sport">` |
| **Bouton radio** | Choisir une seule option dans un même groupe (même `name`). | `<input type="radio" name="sexe" value="F">` |
| **Champ caché** | Transmettre une donnée invisible à l'écran. | `<input type="hidden" name="id" value="25">` |

---

## 3. Autres éléments utiles

### Liste déroulante

Permet de choisir une option parmi plusieurs.

```html
<select name="pays">
  <option value="tn">Tunisie</option>
</select>
```

### Zone de texte

Saisir un texte long : commentaire, remarque.

```html
<textarea name="remarque" rows="4" cols="30"></textarea>
```

### Étiquette (label)

Donne un intitulé à un champ. L'attribut `for` doit correspondre à l'`id` du champ.

```html
<label for="nom">Nom :</label>
<input id="nom" type="text">
```

### Groupe de champs

Regroupe des champs liés. La balise `legend` donne un titre au groupe.

```html
<fieldset>
  <legend>Coordonnées</legend>
  ...
</fieldset>
```

### Boutons

- `submit` envoie le formulaire.
- `reset` réinitialise les champs.
- `button` sert à une action personnalisée.

```html
<input type="submit" value="Envoyer">
<input type="reset" value="Effacer">
<button type="button">Clique</button>
```

---

## 4. Attributs fréquents

| Attribut      | Utilité                                          | Exemple                   |
|---------------|--------------------------------------------------|---------------------------|
| `name`        | Nom envoyé avec la valeur du champ.              | `name="nom"`              |
| `id`          | Identifiant unique, utile avec `label` et CSS.   | `id="nom"`                |
| `value`       | Valeur du champ ou valeur envoyée.               | `value="Tunis"`           |
| `placeholder` | Texte indicatif affiché dans un champ vide.      | `placeholder="Votre nom"` |
| `required`    | Rend la saisie obligatoire.                      | `required`                |
| `checked`     | Coche par défaut une case ou un bouton radio.    | `checked`                 |
| `disabled`    | Désactive un champ.                              | `disabled`                |

---

## 5. Exemple complet

Ce petit formulaire réunit plusieurs éléments étudiés dans cette fiche.

```html
<form action="#" method="post">
  <label for="prenom">Prénom :</label>
  <input type="text" id="prenom" name="prenom" required>
  <br>
  <label for="email">E-mail :</label>
  <input type="email" id="email" name="email">
  <p>Niveau :</p>
  <input type="radio" name="niveau" value="debutant"> Débutant
  <input type="radio" name="niveau" value="avance"> Avancé
  <p>Remarque :</p>
  <textarea name="remarque"></textarea>
  <br>
  <button type="submit">Envoyer</button>
</form>
```

> **À retenir :** chaque champ doit avoir un `name` pour que sa valeur soit transmise. Utilisez `label` pour rendre le formulaire plus clair et plus accessible. Les champs radio d'un même choix doivent partager le même attribut `name`.
