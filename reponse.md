1) Il contient toute la config nécessaire pour versionner, différents 
répertoires
```yml
Gk
Hooks (pour personnaliser)
Info/exclude (exclure des fichiers)
Objects
Refs/heads ; refs/tags
config : configuration 
```
Cela permet d'initier le répertoire (métadonnées et base de données d'objets du projet) et de pouvoir sauvegarder par la suite tout le contenu de nos fichiers déjà archivés

2) - Fichier `untracked`: Le fichier existe, mais git ne suit pas son évolution  = pas de versionning
- Fichier `staged`: le fichier a été au versionning de git, il peut suivre son évolution mais les changements n'ont pas été sauvegardé.
- Fichier `"committed"` : les changements ont été sauvegardés dans notre propre base de donnée.

3) `git diff`: montre le changement entre le répertoire de travail et la zone de staging
-> utilité: quand on veut voir les changements mais pas encore préparé dans la zone de staging
`git diff --staged`: montre le changement entre la staging et le dernier commit
-> utilité: quand on veut voir la différence entre le dernier commit et ce qui n'est pas encore commité 

4) `reset`: permet de revenir a l'état précédent sans créer de nouveau commit
-> Ne pas être de nouveau commit
`revert`: revenir à l'état précédent en créant un nouveau commit
-> quand on veut montrer le changement d'état

5) `fast-forward` : mode de fusion qui vise à aplanir l'historique intégré. Possible lorsqu'aucune divergence n'existe entre les branches.
-> Git va simplement bouger le pointeur de la branche sur le nouveau commit de la branche mergé.
