# Scénario de déploiement odoo 

Ce document décrit quelques lignes directrices pour un déploiement progressif d'odoo 13 community dans une petite ou une moyenne entreprise (PME/PMI). Il est structuré sous forme d'activités d'apprentissage destinées au utilisateurs finaux et dédiées à chaque module.

## Prérequis 

- une installation propre d'odoo ERP. Pour un deployment avec docker consulter [setup odoo on docker.](https://enlight-me.github.io/docker-usecases/setup-images-on-docker/odoo-on-docker.html) 
- préconfiguration et personnalisation d'odoo selon les spécificités de l'entreprise, particulièrement la **création des comptes utilisateurs pour chaque apprenant**. Pour plus de détails consulter la section [configuration](./odoo-deploy-guidelines-fr.md#configuration).

## Sommaire
- [Module Messages](#module-messages)
- [Module Employés](#module-employés)

## Hypothèses
- Petite ou Moyenne Entreprise/Industrie (PME/PMI) de 20 personnes.
- Le déploiement final se feait de manière progressive (par module) avec une durrée d'absorption d'au moins **deux (02) semaines**. 
- Groupes de 8 à 10 apprenants ayant chacun mis à jour son profil utilisateur.
- Processus métier simples. 
- Outils de collaboration : tableau blanc, post-it, marqueurs, ... 
- Equipe projet composé d'un chef de projet et de membres ayant une autorité suffisante sur les activités qui seront implémentées (RH, Stocks, Ventes, ...) 

# Module Messages 

Les activités d'apprentissage de ce module sont : 
1. lister les départements / fonctions / projets existants dans l'entreprise et constituer des groupes dont les conversations sont privés selon la liste ci-dessus.
1. définir les interactions entre les différents groupes.
1. définir des sujets de discussions directes entre deux (02) interloculteurs. 
1. définir les types d'informations dont la diffusion est générale à tous les employés.

Pour chaque activité, créer les cannaux correspondants et produire du contenu (texte, emojis, fichiers attachés, ...).

# Module Employés

Les activités d'apprentissage de ce module sont : 
1. identifier la hiérarchie des structures existantes dans l'entreprise et les postes de travail.
1. créer les départements.
1. créer les postes de travail.
1. créer des employés gestionnaires et les associés aux départements.
1. créer des employés collaborateurs.
1. identifier les parcours (plans) standards des employés dans l'entreprise et les renseigner.
1. lancer des plans sur des employés.
1. associés des employés à des comptes utilisateurs et inviter les à se connecter.
    1. lancer des conversations directes avec ces employés.
    1. vérifier les informations affichées à ces utilisateurs dans leur annuaire des salariés.

# Module Stock

Les activités d'apprentissage de ce module sont : 
1. identifier **sur papier** tous les articles gérés par l'entrprise (consommables, services, produits finis), ainsi que leurs emplacements (entrpots, étagères).
1. mettre à jour les informations de l'entrepot de l'entreprise.
1. identifer les types d'opérations standards dans l'entreprise et les renseigner.
1. identifer les catégories d'articles gérés par l'entreprise et les renseigner.
1. renseigner les informations relatives à au moins 10 articles gérés par l'entreprise avec leurs quantités réels.
1. définir les règles de réapprovisionnement pour chaque article.
1. exécuter quelque opérations manuelles sur les stocks en suivant les mises à jour du tableau de bord **_Vue d'ensemble_** :
    1. transferts pour chaque type d'opération (passer par tous les états)
    1. inventaire en modifiant manuellement les quantités disponibles afin de constater les changements. Passer par tous les états jusqu'à la validation.
    1. rebuter quelques articles et vérifier les changements dans les stocks.
1. exécuter les **_Analyse_** et visualiser les résultats sous différentes formes (liste, tableau, graphes).     

## Exercices avancés module stock

Activer un à un les options suivantes et constater les améliorations apportés :
1. les variantes d'articles
1. les unités de mesures
1. le conditionnement des produits
1. les emplacements de stockage
1. le multi-entrepots
1. les routes en plusieurs étapes 


# Module Facturation

Les activités d'apprentissage de ce module sont : 
1. identifier **sur papier** tous les paramètres liés à la facturation utilisés par l'entrprise, tel que : 
    - les taxes applicables.
    - les termes et conditions de vente.
    - les catégories de conditions de paiement (délais, montant global/partiel, ...)
    - les journaux comptables.
    - les comptes bancaires.
    - les intermédaires de paiements.
    - les pièces réccurentes (frais bancaires, ..). 
1. en groupe, mettre à jour les paramètres du module avce les données collectés.
1. pour les parties factures clients/fournisseurs :
    - lister au moin 10 clients/fournisseurs de l'entreprise et renseigner leurs informations.
    - ajouter des **articles** vendus/achetés par l'entreprise dans la section correspondante (voir module [Stock](./odoo-mod-stock-fr.md) pour plus de détails)
    - créer de nouvelles **factures** pour chaque client/fournisseur, enregister des paiements et marqué les comme comptabilisé.
    - créer de nouveaux **avoirs** pour chaque client/fournisseur, enregister des paiements et marqué les comme comptabilisé.
    - créer de nouvelles **réceptions** pour chaque client/fournisseur, enregister des paiements et marqué comme comptabilisé.
    - créer de nouveaux **paiement** manuels et marqué les comme Validés.
1. A chaque étape consulter le pannaux **Analyse** pour constater l'effet des changements opérés.

     

