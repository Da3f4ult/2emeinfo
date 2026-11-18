# Récapitulatif des éléments d'un formulaire HTML

Chaque élément est présenté avec son rôle, un exemple de code et une **boîte de test** que tu peux utiliser directement.

> **Pour que les boîtes de test fonctionnent :** ouvre ce fichier dans un aperçu Markdown qui accepte le HTML (VS Code → `Ctrl+Shift+V`, Typora, Obsidian…). Certains sites (GitHub par exemple) bloquent les champs de formulaire dans le Markdown.

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

### Texte
Saisir un texte court : nom, prénom.

```html
<input type="text" name="nom" placeholder="Votre nom">
```

<fieldset><legend>Test</legend>
<input type="text" name="nom" placeholder="Votre nom">
</fieldset>

### Mot de passe
Saisir un mot de passe ; les caractères sont masqués.

```html
<input type="password" name="mdp">
```

<fieldset><legend>Test</legend>
<input type="password" name="mdp">
</fieldset>

### E-mail
Saisir une adresse e-mail. Le navigateur peut vérifier son format.

```html
<input type="email" name="email">
```

<fieldset><legend>Test</legend>
<input type="email" name="email" placeholder="nom@exemple.com">
</fieldset>

### Nombre
Saisir une valeur numérique. On peut ajouter `min`, `max` et `step`.

```html
<input type="number" name="age" min="1" max="100">
```

<fieldset><legend>Test</legend>
<input type="number" name="age" min="1" max="100">
</fieldset>

### Téléphone
Saisir un numéro de téléphone.

```html
<input type="tel" name="telephone">
```

<fieldset><legend>Test</legend>
<input type="tel" name="telephone" placeholder="+216 ...">
</fieldset>

### Adresse web
Saisir une adresse internet.

```html
<input type="url" name="site">
```

<fieldset><legend>Test</legend>
<input type="url" name="site" placeholder="https://">
</fieldset>

### Recherche
Champ destiné à une recherche.

```html
<input type="search" name="recherche">
```

<fieldset><legend>Test</legend>
<input type="search" name="recherche" placeholder="Rechercher...">
</fieldset>

### Date
Choisir une date dans un calendrier.

```html
<input type="date" name="date_naissance">
```

<fieldset><legend>Test</legend>
<input type="date" name="date_naissance">
</fieldset>

### Heure
Choisir une heure.

```html
<input type="time" name="heure">
```

<fieldset><legend>Test</legend>
<input type="time" name="heure">
</fieldset>

### Fichier
Sélectionner un fichier sur l'appareil.

```html
<input type="file" name="document">
```

<fieldset><legend>Test</legend>
<input type="file" name="document">
</fieldset>

### Couleur
Choisir une couleur.

```html
<input type="color" name="couleur">
```

<fieldset><legend>Test</legend>
<input type="color" name="couleur">
</fieldset>

### Curseur
Choisir une valeur à l'aide d'un curseur.

```html
<input type="range" name="niveau" min="0" max="10">
```

<fieldset><legend>Test</legend>
<input type="range" name="niveau" min="0" max="10">
</fieldset>

### Case à cocher
Cocher zéro, une ou plusieurs options.

```html
<input type="checkbox" name="interets" value="sport">
```

<fieldset><legend>Test</legend>
<input type="checkbox" name="interets" value="sport"> Sport
<input type="checkbox" name="interets" value="musique"> Musique
<input type="checkbox" name="interets" value="lecture"> Lecture
</fieldset>

### Bouton radio
Choisir une seule option dans un même groupe (même `name`).

```html
<input type="radio" name="sexe" value="F">
```

<fieldset><legend>Test</legend>
<input type="radio" name="sexe" value="F" checked> Féminin
<input type="radio" name="sexe" value="M"> Masculin
</fieldset>

### Champ caché
Transmettre une donnée invisible à l'écran.

```html
<input type="hidden" name="id" value="25">
```

<fieldset><legend>Test</legend>
<form method="get" action="#">
<input type="hidden" name="id" value="25">
Aucun élément visible dans la page. Clique sur le bouton et regarde l'URL : elle doit contenir <code>?id=25</code>.
<br>
<button type="submit">Envoyer</button>
</form>
</fieldset>

---

## 3. Autres éléments utiles

### Liste déroulante
Permet de choisir une option parmi plusieurs.

```html
<select name="pays">
  <option value="tn">Tunisie</option>
</select>
```

<fieldset><legend>Test (quelques options ajoutées)</legend>
<select name="pays">
<option value="">Choisir une option</option>
<option value="tn">Tunisie</option>
<option value="fr">France</option>
<option value="dz">Algérie</option>
</select>
</fieldset>

### Zone de texte
Saisir un texte long : commentaire, remarque.

```html
<textarea name="remarque" rows="4" cols="30"></textarea>
```

<fieldset><legend>Test</legend>
<textarea name="remarque" rows="4" cols="30" placeholder="Écrivez votre remarque..."></textarea>
</fieldset>

### Étiquette (label)
Donne un intitulé à un champ. L'attribut `for` doit correspondre à l'`id` du champ.

```html
<label for="nom">Nom :</label>
<input id="nom" type="text">
```

<fieldset><legend>Test (clique sur le mot « Nom » : le champ est sélectionné)</legend>
<label for="nom">Nom :</label>
<input id="nom" type="text">
</fieldset>

### Groupe de champs
Regroupe des champs liés. La balise `legend` donne un titre au groupe.

```html
<fieldset>
  <legend>Coordonnées</legend>
  ...
</fieldset>
```

<fieldset><legend>Coordonnées</legend>
<label>Nom : <input type="text" name="nom_groupe"></label>
<br>
<label>Téléphone : <input type="tel" name="tel_groupe"></label>
</fieldset>

### Boutons
- `submit` envoie le formulaire.
- `reset` réinitialise les champs.
- `button` sert à une action personnalisée.

```html
<input type="submit" value="Envoyer">
<input type="reset" value="Effacer">
<button type="button">Clique</button>
```

<fieldset><legend>Test (écris dans le champ, puis clique sur « Effacer »)</legend>
<form method="get" action="#">
<input type="text" name="essai" placeholder="Écris quelque chose">
<br>
<input type="submit" value="Envoyer">
<input type="reset" value="Effacer">
<button type="button">Clique</button>
</form>
</fieldset>

---

## 4. Attributs fréquents

| Attribut      | Utilité                                               | Exemple                    |
|---------------|-------------------------------------------------------|----------------------------|
| `name`        | Nom envoyé avec la valeur du champ.                   | `name="nom"`               |
| `id`          | Identifiant unique, utile avec `label` et CSS.        | `id="nom"`                 |
| `value`       | Valeur du champ ou valeur envoyée.                    | `value="Tunis"`            |
| `placeholder` | Texte indicatif affiché dans un champ vide.           | `placeholder="Votre nom"`  |
| `required`    | Rend la saisie obligatoire.                           | `required`                 |
| `checked`     | Coche par défaut une case ou un bouton radio.         | `checked`                  |
| `disabled`    | Désactive un champ.                                   | `disabled`                 |

**Boîte de test des attributs :**

```html
<form method="get" action="#">
  <input type="text" name="ville" value="Tunis">
  <input type="text" name="nom" placeholder="Votre nom" required>
  <input type="checkbox" name="accepte" checked> Coché par défaut
  <input type="text" value="Champ désactivé" disabled>
  <button type="submit">Envoyer</button>
</form>
```

<fieldset><legend>Test (laisse le champ « nom » vide et clique sur Envoyer : le navigateur bloque)</legend>
<form method="get" action="#">
<input type="text" name="ville" value="Tunis"> ← <code>value</code>
<br>
<input type="text" name="nom" placeholder="Votre nom" required> ← <code>placeholder</code> + <code>required</code>
<br>
<input type="checkbox" name="accepte" checked> Coché par défaut ← <code>checked</code>
<br>
<input type="text" value="Champ désactivé" disabled> ← <code>disabled</code>
<br>
<button type="submit">Envoyer</button>
</form>
</fieldset>

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

<fieldset><legend>Test (méthode get pour voir les valeurs dans l'URL)</legend>
<form action="#" method="get">
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
</fieldset>

> **À retenir :** chaque champ doit avoir un `name` pour que sa valeur soit transmise. Utilisez `label` pour rendre le formulaire plus clair et plus accessible. Les champs radio d'un même choix doivent partager le même attribut `name`.