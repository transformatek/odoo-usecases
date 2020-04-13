# Scénario de déploiement pour une gestion par projet

Ce document décrit quelques lignes directrices pour un déploiement progressif d'odoo 13 community dans une petite ou moyenne entreprise/industrie (PME/PMI) dont la gestion est **orientée Projets**. 

Il est structuré sous forme d'activités d'apprentissage destinées aux utilisateurs finaux et dédiées à chaque module.

## Prérequis 

- une installation propre d'odoo ERP. Pour un deployment avec docker consulter [setup odoo on docker.](https://enlight-me.github.io/docker-usecases/setup-images-on-docker/odoo-on-docker.html) 
- préconfiguration et personnalisation d'odoo selon les spécificités de l'entreprise, particulièrement la **création des comptes utilisateurs pour chaque apprenant**. Pour plus de détails consulter la section [configuration](./odoo-deploy-guidelines-fr.md#configuration).

## Sommaire
* [Hypothèses](#hypothèses)
* [Module Messages](#module-messages)
* [Module Employés](#module-employés)
* [Module Vente](#module-vente)
* [Module Projet - activités de base](#module-projet- )
* [Module Projet - activités avancés](#module-projet-activités-avancées)
* [Modules additionnels](#modules-additionnels)
    * [Module Scrum](#module-scrum)
    * [Module Support](#module-support)

## Hypothèses
- Petite ou Moyenne Entreprise/Industrie (PME/PMI) de 20 personnes.
- Le déploiement final se feait de manière progressive (par module) avec une durrée d'absorption d'au moins **deux (02) semaines**. 
- Groupes de 8 à 10 apprenants ayant chacun mis à jour son profil utilisateur.
- Processus métier simples et maturés. Si les processus n'existent pas il faudra les crées. 
- Outils de collaboration : tableau blanc, post-it, marqueurs, ... 
- Equipe projet composé d'un chef de projet et de membres ayant une autorité suffisante sur les activités qui seront implémentées.

## Module Messages 

Les activités d'apprentissage de ce module sont : 
1. lister les départements / fonctions / projets existants dans l'entreprise et constituer des groupes dont les conversations sont privés selon la liste ci-dessus.
1. définir les interactions entre les différents groupes.
1. définir des sujets de discussions directes entre deux (02) interloculteurs. 
1. définir les types d'informations dont la diffusion est générale à tous les employés.

Pour chaque activité, créer les cannaux correspondants et produire du contenu (texte, emojis, fichiers attachés, ...).

[Retour au sommaire](#sommaire)

## Module Employés

Les activités d'apprentissage de ce module sont : 
1. identifier la hiérarchie des structures existantes dans l'entreprise et les postes de travail.
1. créer les départements.
1. créer les postes de travail.
1. créer des employés gestionnaires et les associés aux départements.
1. créer des employés collaborateurs.
1. associés des employés à des comptes utilisateurs et inviter les à se connecter.

[Retour au sommaire](#sommaire)

## Module Vente

Les activités d'apprentissage de ce module sont : 
1. identifier **sur papier** puis mettre à jours les paramètres suivants : 
    1. caractéristiques principales des articles vendus par l'entreprise ainsi que les éventuelles variantes.
    1. créer des comptes utilisateurs pour les commerciaux de l'entreprise, puis intégrer les dans des équipes commerciales.
1. selon le cas, renseigner au moins 10 **articles** vendus par l'entreprise, ainsi que 10 **clients**.
1. créer au moins 05 **devis** avec toutes les informations nécessaires y compris des articles optionnels. Imprimer-les et envoyer-les par mail puis Confirmer-les.
1. créer des **factures** pour les bon de commandes.

[Retour au sommaire](#sommaire)

## Module Projet - activités de base

Les activités de base d'apprentissage de ce module sont :
1. identifier **sur papier** puis mettre à jours les paramètres suivants : 
    1. Types d'activités.
    1. Etiquettes des taches. 
1. si nécessaire, créer des employés pour les membres des équipes projets de l'entreprise et leur associés des utilisateurs.
1. si nécessaire, renseigner au moins 05 clients.
1. créer au moins 02 projets et renseigner les informations y relatives.
1. ajouter des pièces jointes de différents formats aux projets.
1. dans la partie **Projets** sélection un des projets :
    1. ajouter des colonnes (TODO, WIP, DONE).
    1. paramétrer chaque colone.
1. ajouter des tâches dans chaque étape du projets.
1. faite glisser les taches entre les différentes étapes et constater les changments dans la partie analyse.
1. editer les tâches et renseigner les informations y relatives.
1. modifier l'état des tâches et constater le indicateurs couleurs sur le kanban projet et dans la partie **Toutes les taches**. 

## Module projet - activités avancées

Les activités de base d'apprentissage avancées de ce module sont :
1. identifier **sur papier** les éléments suivants : 
    1. projets en cours au niveau de l'entreprise.
    1. tâches relatives à chaque projet.
    1. sous-taches des taches listées ci-avant.

1. avec l'option **_Sous-tâches_** activé dans la configuration :
    1. renseigner les informations relatives à un des projets identifiés.
    1. renseigner les tâches du projet.
    1. créer les sous-tâches en les reliants à leurs taches parentes.
    1. assigner les taches/sous-tâches à des membres de l'équipe.
    1. chaque membre constate la liste des tâches qui lui sont assignés et les fait progrésser dans le pipeline.
    1. refaire l'opération pour les autres projets identifiés.
    1. créer une hiérarchie de projets en les reliants avec le champ **_Sous-tache du projet_**.

1. avec l'option **_Utiliser les évaluations de projet_** activé dans la configuration :
    1. **cette option nécessite des informations client fiables, ainsi que la configuration d'un serveur de messagerie et/ou l'accès client au portail de l'entreprise**.
    1. pour l'un des projets identifiés, définir un **_Modèle d'email pour les évaluations_** pour chaque étape.
    1. le client recevra un email de demande d'evaluation chaque fois q'une tâche progresse dans le pipeline et les feedbacks seront visibles directement dans la vue kanban du projets avec chaque tâche.

1. avec l'option **_Feuilles de temps sur les tâches_** activé dans la configuration.
    1. pour l'un des projets identifiés, activé l'option **_Feuilles de temps_**.
    1. créer un nouveau modèle de **Temps de travail** adapté à la législation locale (Heures de travail, Congé Global).
    1. renseigner le **_Coût de la feuille de temps_** pour chaque membre de l'équipe (module employés).
    1. pour chaque tâche du projet selectionnée, renseigner le champ **_Heures planifiées_**.
    1. les membres d'équipes peuvent maintenant renseigner leurs apports en volume horaire à chaque tâche et visualiser les heures restantes dans la vue kanban du projet.
    1. visualiser les changements dans la partie analyse après chaque modification sur les horaires travailés par employé / par tache / par projet. 
    1. dans le module **_Feuilles de temps_** :
        1. chaque membre de l'équipe visulise ses feuilles de temps.
        1. visualiser la liste de toutes les feuilles de temps.
        1. faite des analyses par employé / par tache / par projet.
        1. changer l'option **_Unité d'encodage_** dans la configuration et visualiser les modifications apportées aux informations projets / taches / feuilles de temps du module Projet.
    1. refaire l'opération pour les autres projets identifiés.

1. dans le cas où le module vente est installé, on peut définir **_Créer un bon de commande_** directement à partir de la page de configuration du projet
    1. dans le module vente créer des articles de type service et configurer la **_Politique de facturation du service_** sur **_Feuilles de temps sur les tâches_**.
    1. un service pour chaque type d'employé ????
    1. 

comment facturer les feuilles de temps. ???

Facturation des horaires travailés



[Retour au sommaire](#sommaire)

## Modules additionnels 

### Module Scrum 

### Module Support


----
[Sommaire général](./odoo-deploy-guidelines-fr.md)