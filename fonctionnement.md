installation de django : pip install django
pour la version :django-admin --version
Creation du projet django : django-admin startproject my_blog

pour lancer le serveur : python manage.py runserver

django fonctionne suivant les applications (package)
pour le faire : python manage.py startapp app_name

django fonctionne suivant le principe MVT = Model View Template 
Models = Données ; Views = Function ; template =  Afficharge des données

il faut ecrire des urls qui appel des functions appele des données et les données sont afficher au niveau de templates

urls => route
view => controller
template => la vue

connexion espace admin
- commencer par la migration : python manage.py migrate
- creer un superUserb : python manage.py createsuperuser --username admin --email admin@yahoo.fr

Creation des models 
pour le faire on se doit de creer une class et le systeme ORM va permettre d'injecter cette classe dans notre base de données . django à deja un module model et notre nouvelle classe va etendre de ce model.

prendre le fichier models.py creer la class qui va representer la table etva etendre models.Model 
creer tous les champs de la tables 
lancer la commande pour creer la migration :python manage.py makemigrations
pour gerer les champs images django a besoin Pillow : python -m pip install Pillow 

creer dans la base de données avec :python manage.py migrate

dans  le fichier admin.py enregistrons article afin de l'afficher dans notre espace d'administration 


** Afficher les données depuis la base de donées
prendre le fichier views et y importé la table
