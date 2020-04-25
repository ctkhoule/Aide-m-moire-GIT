# Aide-memoire GIT
Git est le sytème de gestion de version décentralisé open source qui facilite les activités GitHub sur votre ordinateur.
Cet aide-mémoire permet un accès rapide aux instructions des commandes Git les plus utilisées.

## Configuration des outils
Configurer les informations de l'utilisateurs pour tous les dépôts locaux

- Définit le nom que vous voulez asocier à toutes vos opérations de commit :

  `git config --global user.name "votre nom"`
  
- Définit l'email que vous voulez associer à toutes vos opérations de vommit :
  
  `git config --global user.email "adresse email"`
    
- Active la coloration de la sortie en ligne de commande :

  `git config --global color.ui auto`
 
 - Voir la configuration :
 
   `git config --list`
   
## Créer dépôt et fichier .gitignore
Démarrer un nouveau dépôt ou en obtenir un depuis une URL existante et créer un fichier « .gitignore » 

- Créer un dépôt local à partitr du nom spécifié :

   `git init nom-du-projet`
   
 - Créer un nouveau dépôt local (dans le dossier courant) :
 
    `git init`
  
 - Cloner un dépôt existant : 
 
    `git clone url`
  
  - Créer un fichier « .gitignore » :
  
    `vim .gitignore`
   
    `git add .gitignore`
   
    `git commit -m "Ajout fichier gitignore"`
    
 - Créer un fichier « .gitignore » en utilisant un template « Windows » :
 
    `curl -s https://www.gitignore.io/api/windows > .gitignore`
    
    `git add .gitignore`
    
    `git commit -m "Ajout gitignore"`
 
- Créer un fichier « .gitignore » en utilisant un template « MacOS » :

    `curl -s https://www.gitignore.io/api/osx > .gitignore`

    `git add .gitignore`

    `git commit -m "Ajout gitignore"`
   
## Effectuer des changements
Consulter les modifications et effectuer une opération de commit

- Liste tous les nouveaux fichiers et les fichiers modifiés à commiter :

    `git status`
    
- Montre les modifications de fichiers qui ne sont pas indexés :

    `git diff`
    
- Montre les diférence de fichiers entre la version indexée et la dernière version :

    `git diff --staged`
    
- Enleve le fichier de l'index, mais conserve son contenu :

    `git reset nom-fichier`
    
- Ajoute tous les changements de toute l'arborescence

    `git add --all`
    
- Ajoute un instantané du fichier, en préparation pour le suivi de version :
 
    `git add nom-fichier`
    
- Enregistre des instantanés de fichiers de façon permanente dans l'historique des versions :

    `git commit -m "message du commit"`
    
- Premier commit :

    `git add .`

    `git commit -m "Initial commit"`
    
- Commit suivant :

    `git add chemin-vers-mon-fichier`

    `git commit -m "message du commit"`
    
- Modifie le commit précédent : 

    `git commit --amend -m "nouveau message du commit"`
    
## Grouper des changements - les branches & tags
Nommer une série de commits et combiner les résultats de travaux terminés

- Liste toutes les branches dans le dépôt courant :

    `git branch`
    
- Crée une nouvelle branche :

    `git branch nom-branche`
    
- Bascule sur la branche spécifiée :

    `git checkout nom-branch`
    
- Crée et bascule sur la nouvelle branche :

    `git checkout -b nom-branche`
    
- Renomme la branche en cours :

    `git branch -m nouveau-nom-branche`
    
- Supprime une branche spécifiée :

    `git branch -d nom-branche`
    
- Combine dans la branche courante l'historique de la branche spécifiée :

    `git merge nom-branche`
    
- Crée une nouvelle branche de suivi, basée sur une branche distante :

    `git branch --track nouvelle-branche branche-distante`
    
- Marque le commit courant avec un tag :

    `git tag nom-tag`
    
## Vérifier l'historique des versions
Suivre et inspecter l'évolution des fichiers du projet

- Montre l'historique des versions pour la branche courante :

    `git log`
    
- Montre l'historique des versions, y compris les actions de renommage, pour le fichier spécifié :

    `git log --follow nom-fichier`
    
- Affiche tous les commits (uniquement l'identifiant et le texte) :

    `git log --oneline`
    
- Affiche l'historique d'un utilisateur uniquement :

    `git log --author="nom utilisateur"`
    
- Affiche l'historique des modifications pour un fichier uniquement :

    `git log -p nom-fichier`
    
- Affiche les changements en détails dans un fichier :

     `git blame nom-fichier`
     
- Montre les modificaions de métadonnées et le contenu inclues dans le commit spécifié :

     `git show identifiant-du-commit`
     
- Affiche X derniers commits :

     `git log -n X`

## Changement au niveau des noms de fichiers
Déplacer et supprimer des fichiers sous suivi de version

- Supprime le fichier du répertoire de travail et met à jour l'index :

    `git rm nom-fichier`
   
- Supprime le fichier du système de suivi de version mais le préserve localement :

    `git rm --cached nom-fichier`
  
- Renomme le fichier et prépare le changement pour un commit :

    `git mv nom-fichier nouveau-nom-fichier`
  
  ## Refaire des commits
  Corriger des erreurs et gérer l'historique des corrections
  
- Annule tous les commits après 'identidifiant-du-commit', en coservant les modifications localement :
  
    `git reset identifiant-du-commit`
  
- Supprime tout l'historique et les modifications effectuées après le commit spécifié :

    `git reset --hard identifiant-du-commit`

## Enregistrer des fragments
Mettre en suspens des modifications non finies pour y revenir plus tard

- Enregistre de manière temporaire tous les fichiers sous suivi de version qui ont été modifiés ("remiser son travail") :

    `git stash`
    
- Applique une remise et la supprime immédiatement :

    `git stash pop`
    
- Liste tous les remises :

    `git stash list`
    
- Supprime la remise la plus récente :

    `git stash drop`







