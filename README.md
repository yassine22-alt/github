## Scénario #1

### 1. First step: Immersion
1) Git est un système de gestion de versions distribué qui permet de suivre les modifications du code, de collaborer avec d'autres développeurs et de gérer différentes versions d'un projet de manière efficace.

2) Le dossier .git est un répertoire caché créé lorsqu'on initialise un dépôt Git (git init). Il contient toutes les informations nécessaires pour suivre l'historique du projet. (HEAD, config, commits,...)

3) Les commentaires dans Git, principalement via les messages de commit, permettent de clarifier les modifications, améliorer la collaboration, faciliter le débogage et documenter l'évolution du projet.

4) Commandes utilisees: 
`git add .`
`git commit -m "demo commit test"`
`git remote add origin https://github.com/yassine22-alt/github.git`

### 2. Second step: Découverte

1) - HEAD est un pointeur qui indique la référence actuelle dans Git. Il pointe généralement vers la dernière commit de la branche active.
   - Les logs enregistrent l’historique des commits et des actions Git. Ils permettent de retracer les modifications effectuées.
   - Une branche est une version parallèle du code, permettant de     travailler sur des fonctionnalités sans affecter le projet principal.
2) `git add .`
`git commit -m "licence added"`

3) Pour afficher les fichiers traqués par Git : `git ls-files`


### 3. Third step: Historique
1) `git log --oneline --graph -1`
2) To make it as an alias `git config --global alias.historic "log --oneline --graph -1"`
3) List alias : `git config --global --list | grep alias`
4) Historic of README file: `git historic projects/demo/README.md`


### 4. Fourth step: Exclusion des fichiers
1) Staging sans utiliser `git add .` : `git commit -am "staging without adding"`


### 5. Fifth step: Branching and Merging
1) Créer une branche updates, effectuer le staging et le commit en une seule ligne : `git checkout -b updates && git add . && git commit -m "Initial commit on updates"` 
2) `git merge updates`


### 6. Sixth step: Résolution de conflits

J'ai d'abord créé une branche BAD, puis ajouté la section "Trouble" dans le fichier README.md. Ensuite, j'ai basculé sur la branche main et ajouté la section "Troubleshooting". Après cela, j'ai fusionné la branche main avec la branche bad. Lors de la fusion, un conflit a été détecté dans le fichier README.md, que j'ai résolus manuellement avant de valider le merge par un commit.


## Scénario #2

### 1. First step: Tagging

1) `git tag -a V1.0 -m "RELEASE 1.0"`
2) `git show V1.0`
3) Les tags marquent des versions spécifiques dans l'historique du projet, comme des versions stables ou des releases. Ils permettent de :

Identifier clairement des versions importantes (ex. V1.0).
Faciliter le déploiement et les tests.
Avoir un historique lisible pour retrouver facilement des points fixes dans le projet.

### 2. Second step: Stashing et sauvegarde du travail en cours

1) `git stash `permet de mettre temporairement de côté (stocker) les modifications non commises dans votre répertoire de travail, afin de revenir à un état propre (sans perdre vos modifications).