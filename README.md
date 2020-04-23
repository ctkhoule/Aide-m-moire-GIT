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

- Liste tous les nouveaux fihiers et les fichiers modifiés à commiter :

    `git status`
    
- Montre les modifications de fichiers qui ne sont as indexés :

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

    

    




