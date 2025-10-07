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



** Exercice N°2:

![](./assets/2_1.png)

![](./assets/2_2.png)



** Exercice N°3

![](./assets/3_1.png)

![](./assets/3_2.png)

![](./assets/3_3.png)

![](./assets/3_4.png)


