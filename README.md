# Site officiel du Centre Spatial Étudiant de l'École Polytechnique 

Trouvez le lien [ici](http://astronautix-cse-polytechnique.github.io/)

# Pour proposer un article

## Redaction

Les articles s'écrivent en [Markdown](http://www.wikiwand.com/fr/Markdown), une syntaxe très simple.
L'entête de l'article doit être comme suit :

	---
	author: votre nom
	comments: false
	date: YYYY-MM-DD HH:MM:SS+00:00
	layout: article
	slug: un-titre-avec-des-tirets
	title: Un titre normal
	category: Une catégorie parmi Evenement ou Miniconf (seules catégories utilisées pour le moment)
	---


## Envoi

Vous pouvez ensuite nous les envoyer ou si vous êtes à l'aise avec Git, nous faire une pull request.êtes à l'aise avec Git, nous faire une pull request.
Un article s'enregistre sous le format YYYY-MM-DD-mon-titre-avec-des-tirets.markdown dans le dossier _posts/

# Pour écrire une page

Faire de même qu'avec un article avec le layout page.
Il s'enregistre sous la forme index.md dans le dossier du nom du lien désiré.

# Pour installer un serveur de test chez soi

Tout d'abord cloner le repository

	git clone https://github.com/astronautix-cse-polytechnique/astronautix-cse-polytechnique.github.io.git

Puis installer Jekyll et ses dépendances (Ruby, Rubygems, nodeJS, Python2.7)

	gem install jekyll

Pour lancer le serveur

	jekyll build
	jekyll serve

Plus d'information sur le site de [Jekyll](http://jekyllrb.com/docs/installation/)
