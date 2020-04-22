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


