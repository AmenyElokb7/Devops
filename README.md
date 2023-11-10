# Mon Projet Git

Ce projet a été créé dans le cadre de l'apprentissage et de la mise en pratique des concepts de base de Git. Les sections suivantes décrivent les étapes que j'ai suivies pour préparer mon environnement, créer un nouveau projet, comprendre les concepts de base de Git, collaborer avec d'autres développeurs, et utiliser GitFlow.

## Partie 1: Préparation de l'environnement Git

### 1. Génération de la clé SSH

Pour permettre des connexions sécurisées, j'ai généré une clé SSH et l'ai ajoutée à mon compte sur le dépôt distant GitHub.

```bash
ssh-keygen -t rsa -b 4096 -C amenyelokb@email.com
cat ~/.ssh/id_rsa.pub
```

### 2. Configuration de Git
J'ai configuré mon nom d'utilisateur et mon adresse e-mail pour que mes commits soient correctement identifiés.
```bash
git config --global user.name AmenyElokb7
git config --global user.email amenyelokb@email.com
```

### 3. Connexion SSH aux dépôts distants
J'ai testé ma connexion SSH au dépôt distant.
```bash
ssh -T git@github.com
```
## Partie 2: Création d'un nouveau projet
J'ai créé un nouveau projet sur GitHub et noté l'URL du projet.

J'ai cloné le projet sur ma machine locale.

## Partie 3: Concepts de base de Git
### 1. Travailler avec les fichiers
J'ai créé un fichier index.html, ajouté du contenu, puis ajouté et validé mon premier commit.
```bash
touch index.html
echo "Contenu de votre fichier" > index.html
git add index.html
git commit -m "Premier commit : ajout de index.html"
```

### 2. Historique des commits
J'ai visualisé l'historique des commits avec git log et affiché les différences entre deux commits avec git diff.

## Partie 4: Collaborer sur Git
J'ai créé une nouvelle branche pour travailler sur une fonctionnalité spécifique.
```bash
git branch ma-fonctionnalite
git checkout ma-fonctionnalite
```
J'ai effectué des modifications, ajouté et validé un commit, puis poussé les modifications vers le dépôt distant.
Gestion des conflits : J'ai simulé un conflit, résolu le conflit après fusion des branches.
```bash
git add .
git commit -m "Modification de ma-fonctionnalite"
git push origin ma-fonctionnalite
```

## Partie 5: Utilisation de GitFlow
J'ai initié GitFlow et créé une nouvelle fonctionnalité.
```bash
git flow init
git flow feature start ma-fonctionnalite
```
J'ai créé une nouvelle version et fusionné la branche de fonctionnalité dans la branche de développement.
```bash
git flow release start ma-version
git flow feature finish ma-fonctionnalite
```
J'ai créé un correctif avec GitFlow.
```bash
git flow hotfix start mon-correctif
```
