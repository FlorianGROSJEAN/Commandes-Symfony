# Commandes-Symfony

## Création avec composer :

    composer create-project symfony/skeleton nomduprojet


## Démarrage du serveur PHP :

    cd nomduprojet

    php -S localhost:8080 -t public 


## Router avec Annotation : 

    composer require annotations


## Création de la DB

    php bin/console doctrine:database:create

    php bin/console doctrine:database:drop 

## Mettre à jour la DB

    php bin/console doctrine:schema:update --force

### ou par migrations :

    bin/console make:migrations 
    
    puis 

    bin/console doctrine:migrations:migrate


## Création d'une entité

    php bin/console make:entity


## Maker

    composer require --dev symfony/maker-bundle 


## Création d'un controller (src/Controller)

    php bin/console make:controller  


## Twig

### Twig bundle :

    composer require twig

### Twig Asset (pour le css, les images, ...) : 

    composer require symfony/asset


## Fixtures :

### installer le bundle fixtures:

        composer require --dev orm-fixtures

### pour charger les données:    

         php bin/console doctrine:fixtures:load

         php bin/console doctrine:fixtures:load --append (charger sans écraser les données précédentes)


## Faker

    composer require --dev fakerphp/faker

## Créer form 

    bin/console make:form


## Créer User 

    bin/console make:user


## Créer un form de login

    bin/console make:auth

## CRUD 

    bin/console make:crud

## Voter   

    bin/console make:voter

# version JB (@copyright 2021):

composer install
	composer create-project symfony/website-skeleton nomduprojet
	
	mv nomduprojet/* .
	mv nomduprojet/.env* .
	mv nomduprojet/.gitignore* .
	rm -rf nomduprojet/
	
	Modify your DATABASE_URL config in .env
	mysql --version
	explorateur / Ereul9Aeng
	DATABASE_URL="mysql://explorateur:Ereul9Aeng@127.0.0.1:3306/oflix?serverVersion=mariadb-10.3.25"
	
	bin/console doctrine:database:create
	bin/console doctrine:database:drop
	
	php bin/console doctrine:fixtures:load
	php bin/console doctrine:fixtures:load --append
		
	composer require --dev fakerphp/faker
	
	bin/console make:controller
	bin/console make:entity
	bin/console make:crud
	bin/console make:form
	bin/console make:voter
	bin/console make:user
	bin/console make:auth
	bin/console sec:hash
	
	
	bin/console make:migration
	bin/console doctrine:migrations:migrate
	bin/console doctrine:schema:update --force
	
	config/package/twig.yaml :
	form_themes: ['bootstrap_5_layout.html.twig']