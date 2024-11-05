L’exercice suivant correspond à une situation réelle que peut rencontrer un développeur IAD.

Contexte : un de vos collègues vient de se lancer sur un nouveau projet en clean architecture avec une approche DDD, il vous propose de faire la code review de sa 1ère PR. Vous devez mettre en évidence les normes qui ne sont pas respectés et les implémentations techniques qui ne respectent pas les principes de ces approches.

# Glossaire

* Real Estate : Domaine de l'immobilier
* Property : bien à vendre
* Advisor : conseiller en charge de vendre le bien

# Métier

Dans le contexte "Real Estate", un conseiller peut rentrer les informations d'un nouveau bien Property dans le système. La fonctionnalité demandée est d'implémenter une command (Symfony) qui va stocker un nouveau bien en prenant les arguments suivants :

* l'id de la Property
* l'id de l'Advisor qui entre les informations de la Property
 
# Structure des dossiers

```
RealEstate/
    Discovering/
        Property/
            Adapters/
                Controller/
                   Symfony/
                        Command/

            Entities/
                Property/ 

            UseCases/
                Gateways/
                    Property/

                Property/
                    AddPropertyForAdvisor
```

# Technique

Le code a été conçu avec une approche "Clean Architecture" et selon les concepts liés au DDD, le but étant d'isoler et protéger les règles métier

# Restitution

Vous exposerez vos remarques sur la PR pendant 1h à nos lead tech. Ce sera une base de discussion pour échanger de façon plus approfondie sur les problématiques rencontrées


PS : les changement sur la partie readme : 

```
## Technique

Il faut prendre en compte qu'il s'agit de code pour du PHP 7.2.

Les dépendances ainsi que certains fichiers sont manquants, c'est volontaire pour ne pas alourdir la code review. 

Le code a été conçu avec une approche "Clean Architecture" et selon les concepts liés au DDD, le but étant d'isoler et protéger les règles métier

# Objectifs

Mettre en évidence:

* les soucis d'implémentation de la PR ne respectant pas les grands principes de cette architecture

* les erreurs/améliorations de conceptions

* les erreurs liés à des normes de code.

* tout ce qui vous paraît anormal / que vous auriez fait différemment
```
