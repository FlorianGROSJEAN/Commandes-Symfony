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