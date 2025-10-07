* Solution Git/Github


* Exercice N°1:

Aprés avoir telecharger CLI (gh), l'outil qui nous permet de gerer github depuis le terminal, je suis passé sur le terminal comme suit:


* gh auth login : pour connecter le compte github avec terminal


![](./assets/1_1.png)

* ls -al ~/.ssh : pour verifier dans le fichier .ssh si on a deja la clé ssh


* cat ~/.ssh/id_ed25519.public : pour afficher la clé ssh

![](./assets/1_2.png)

* gh ssh-key add ~/.ssh/id_ed25519.pub : pour ajouter la clé ssh a github

* ssh -T git@github.com : pour tester la connexion ssh avec github

![](./assets/1_3.png)

* gh repo create git-learning-1 --public --confirm : pour créer un nouveau repo public sur github avec le nom git-learning-1, et confirmer la création sans poser de question

![](./assets/1_4.png)

* git clone git@github.com:Epiphane-code/git-learning-1.git : pour cloner le repo en local


![](./assets/1_5.png)

* cd git-learning-1 : pour entrer dans le dossier du repo

* echo "Mon premier projet git" > README.md : pour créer un fichier README.md et y ajouter le texte "Mon premier projet git"

* cat README.md : pour afficher le contenu du fichier README.md

* echo "Omar Epiphane Mac 21" >> README.md : pour ajouter le texte "Omar Epiphane Mac 21" dans le fichier README.md

![](./assets/1_6.png)

* git status : pour vérifier l'état du repo et voir les modifications non suivies

* git add README.md : pour ajouter le fichier README.md à l'index (staging area)

* git commit -m "description du commit" : pour valider les modifications avec un message de commit

* git push origin main : pour pousser les modifications vers la branche principale (main) du repo distant sur github

![](./assets/1_7.png)



* Exercice N°2:

* git checkout -b myself : pour créer et basculer sur une nouvelle branche appelée myself

* echo "Omar, Epiphane, Maradi" > about.txt : pour créer un fichier about.txt et y ajouter le texte "Omar, Epiphane, Maradi"

* git status : pour vérifier l'état du repo et voir les modifications non suivies

* git add about.txt : pour ajouter le fichier about.txt à l'index (staging area)

* git commit -m "description du commit" : pour valider les modifications avec un message de commit

* git push origin myself : pour pousser les modifications vers la branche myself du repo distant sur github

![](./assets/2_1.png)

* gh pr create --base main --head myself --title "request" --body "test" : pour créer une pull request depuis la branche myself vers la branche main sur github

* git diff main : pour voir les différences entre la branche actuelle (myself) et la branche main

* git checkout main : pour basculer sur la branche principale (main)

* git pull origin main : pour récupérer les dernières modifications de la branche principale (main) du repo distant sur github

* git merge myself : pour fusionner la branche myself dans la branche principale (main)

* git branch -d myself : pour supprimer la branche myself localement

* git push origin --delete myself : pour supprimer la branche myself du repo distant sur github


![](./assets/2_2.png)



** Exercice N°3

* git repo create git-learning-3 --public --confirm : pour créer un nouveau repo public sur github avec le nom git-learning-3, et confirmer la création sans poser de question

* git clone git@github.com:Epiphane-code/git-learning-3.git

* cd git-learning-3 : pour entrer dans le dossier du repo

* echo "Ligne écrite depuis la branche main" > notes.txt : pour créer un fichier notes.txt et y ajouter le texte "Ligne écrite depuis la branche main"

* git status : pour vérifier l'état du repo et voir les modifications non suivies

* git add notes.txt : pour ajouter le fichier file.txt à l'index (staging area)

* git commit -m "commit" : pour valider les modifications avec un message de commit

* git push origin main : pour pousser les modifications vers la branche principale (main) du repo distant sur github

![](./assets/3_1.png)

* git checkout -b conflict-test : pour créer et basculer sur une nouvelle branche appelée conflict-test

* echo "Ligne écrite depuis conflict-test" >> notes.txt

* git status

* git add notes.txt : pour ajouter le fichier notes.txt à l'index (staging area)

* git commit -m "commit" : pour valider les modifications avec un message de commit

* git checkout main : pour basculer sur la branche principale (main)

* echo "Ligne écrite depuis main pour la seconde fois" >> notes.txt

* cat notes.txt

![](./assets/3_2.png)

* git merge conflict-test : pour fusionner la branche conflict-test dans la branche principale (main), ce qui provoque un conflit

* git status : pour vérifier l'état du repo et voir les fichiers en conflit

* git add notes.txt : pour marquer le fichier notes.txt comme résolu

* git commit -m "com" : pour valider la résolution du conflit avec un message de commit

* git push origin main : pour pousser les modifications vers la branche principale (main) du repo distant sur github

* git merge conflict-test : pour fusionner la branche conflict-test dans la branche principale (main) à nouveau, ce qui ne provoque plus de conflit car il a été résolu

* code notes.txt : pour ouvrir le fichier notes.txt dans l'éditeur de code (VS Code) gerer le conflit

* git status : pour vérifier l'état du repo et voir les modifications non suivies



![](./assets/3_3.png)


* git add notes.txt : pour ajouter le fichier notes.txt à l'index (staging area)

* git commit -m "commit" : pour valider les modifications avec un message de commit

* git push origin main : pour pousser les modifications vers la branche principale (main) du repo distant sur github

![](./assets/3_4.png)


