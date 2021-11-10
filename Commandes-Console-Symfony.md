# Création avec composer :

    composer create-project symfony/skeleton nomduprojet


# Démarrage du serveur PHP :

    cd nomduprojet

    php -S localhost:8080 -t public 


# Router avec Annotation : 

    composer require annotations


# Création de la DB

    php bin/console doctrine:database:create 

# Mettre à jour la DB

    php bin/console doctrine:schema:update --force

    ou par migrations :

    bin/console make:migrations 
    
    puis 

    bin/console doctrine:migrations:migrate


# Création d'une entité

    php bin/console make:entity


# Maker

    composer require --dev symfony/maker-bundle 


# Création d'un controller (src/Controller)

    php bin/console make:controller  


# Twig

    Twig bundle : composer require twig

    Twig Asset (pour le css, les images, ...) : composer require symfony/asset


# Fixtures :

    -installer le bundle fixtures:

        composer require --dev orm-fixtures

    -pour charger les données:    

         php bin/console doctrine:fixtures:load

         php bin/console doctrine:fixtures:load --append (charger sans écraser les données précédentes)


# Créer form 

    bin/console make:form


# Créer User 

    bin/console make:user


# Créer un form de login

    bin/console make:auth

# CRUD 

    bin/console make:crud

## version JB :

php -S 0.0.0.0:8080 -t public

	Modify your DATABASE_URL config in .env

	DATABASE_URL="mysql://explorateur:Ereul9Aeng@127.0.0.1:3306/oflix?serverVersion=mariadb-10.3.25"
	
	composer create-project symfony/website-skeleton nomduprojet
	mysql --version
	php bin/console doctrine:database:create
	php bin/console doctrine:database:drop
	php bin/console make:entity
	php bin/console make:migration
	php bin/console doctrine:migrations:migrate
	php bin/console doctrine:schema:update --force
	explorateur / Ereul9Aeng
	php bin/console make:crud
	php bin/console make:form
	php bin/console make:controller
	
	php bin/console sec:hash
	
	bin/console make:voter
	
	php bin/console doctrine:fixtures:load
	php bin/console doctrine:fixtures:load --append
	
	mv nomduprojet/* .
	mv nomduprojet/.env* .
	mv nomduprojet/.gitignore* .
	rm -rf nomduprojet/
	
	composer require --dev fakerphp/faker

	


	form_themes: ['bootstrap_5_layout.html.twig']