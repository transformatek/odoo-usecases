# Module Stock

Ce document illustre les différentes fonctionnalités du module **Stock** d'odoo 13 community. 

## Présentation du module 

Ce module est destiné à optimisez l'organisation des entrepôts de l'entreprise grâce à un système d'inventaire intelligent de double entrée. Il permet d'optimisez toutes les opérations internes, et d'obtenir la méthode de stockage la plus efficace possible. L'inventaire en double entrée d'Odoo n'a pas de saisie, de sortie ou de transformation de stock. A la place, toutes ces opérations consistent en des mouvements d'inventaire entre les emplacements disponibles.

![](./images/stock-overview.png)

# Configuration (admin)

Cette section, réservée aux **administrateurs** et **Gestionnaires des stocks**, permet de définir les paramètres généraux du module, tel que les opérations (préparation par lots, Colis), les confirmations d'expédition (email, SMS), les options des articles, la traçabilité et les entrepots.

### Configuration des Articles

Cette section permet de définir les paramètres des articles tel que les variantes, les unités de mesures et le conditionnement de produits. 

![](./images/stock-config-article.png)

* les variantes : si cette option est selectionnée, le **gestionnaire des stocks** aura la possibilité de prédéfinir des caractéristiques communes pour les articles (couleur, options, ...). Pour chaque caractéristique un ensemble de valeurs est prédéfini. 

* les unités de mesures : si cette option est sélectionnée, le **gestionnaire des stocks** aura la possibilité de prédéfinir des unités de mesures utilisables pour les articles (km, kg, ...). 

* le conditionnement de produits : si cette option est sélectionnée, le **gestionnaire des stocks** aura la possibilité de prédéfinir des modèles de conditionnement pour les articles (packs de 4/6/8/...). 

### Configuration des Entrepots

Cette section permet de définir les paramètres des entrepots tel que les emplacements, le multi-entrepots et les routes. 

![](./images/stock-config-entrepot.png)

* Emplacements de stockage : si cette option est selectionnée, le **gestionnaire des stocks** aura la possibilité de prédéfinir des emplacements spécifiques dans chaque entrepot pour ranger les articles selon la **_stratégie de rangement définie_**. 

* Multi-Entrepots : si cette option est selectionnée, le **gestionnaire des stocks** aura la possibilité d'ajouter autant d'entrepots qu'il le souhaite. Sinon **un seul** entrepot sera disponible pour le stockage, celui de l'entreprise. 

* Routes en plusieurs étapes : si cette option est selectionnée, le **gestionnaire des stocks** aura la possibilité de prédéfinir des routes (étapes) standards par lesquelles les articles sont acheminés, ainsi que les règles associées.

## Entrepots

Cette section permet de renseigner les informations relatives à l'entrepot principal de l'entreprise et aux autres entrepots si l'option [Multi-Entrepots est activé](#configuration-des-entrepots) (identification, nom sourt, adresse).

## Types d'opérations 

Cette section permet de définir les types d'opérations affectant les stocks tel que la réception et la livraison.

![](./images/stock-type-operation.png)

Les opérations peuvent avoir un code, un type (Reçu, Livraison, Transfert interne) et être associées à des opérations de retours.

## Catérogies d'articles 

Cette section permet de définir une **hiérarchie** des catégories d'articles gérés par l'entreprise, tel que les articles disponibles à la vente, les matières premières, les fournitures, ...

# Données de base

Le menu Données de base permet de resneigner les informations relatives aux **_Articles_** et aux **_Règles de réapprovisionnement_**. 

## Articles 

Cette section permet de renseigner les informations relatives à tous les articles gérés par l'entreprise. 

![](./images/stock-article.png)

Les articles peuvent être vendu et/ou acheté et selon leur type (consommable, service, stockable) des informations relatives à leur stockage peuvent être renseignées.

## Règles de réapprovisionnement 

Les règles de réapprovisionnement définissent, pour chaque article, les quantités min/max ainsi que les délai de réception/achat.

# Opérations 

Le menu opération permet de resneigner les informations relatives aux **_Transferts_**, **_Adjustement de stock_** et les **_Rebuts_**. Il permet aussi de **_lancer le planificateur_** afin de créer les opérations nécessaires au réapprovisionnement des stocks selon les régles prédifinis dans les [Données de base](#données-de-base). 

## Transferts

Les transferts permettent d'exécuter des opérations sur les stocks dont les types sont définis dans [Types d'opérations](#types-dopérations). 

![](./images/stock-transfert.png)

Une fois définie, l'opération passe par en ensemble d'états, identifiables sur la barre en haut, et qui sont : Brouillon, En attente, Pret, Fait. Aussi le transfert peut être annulé à tous moment par le **gestionnaire des stocks**.

**NB**: de manière générale ces transferts sont rarement exécutés manuellement puisqu'ils sont intégrés avec les modules **Achats** pour les réceptions et **Ventes** pour les livraisons. Ils sont aussi utilisés par le module **_Compatabilité_**. 

## Adjustement de stocks

Les adjusments de stocks sont réallisés dans le cadre **d'inventaires** périodiques et affectes un ou plusieurs articles gérés par l'entreprise. Pour ce faire il faut créer un nouveau **_inventaire_** (Référence, articles concernés) et le **_démarrer_**.

![](./images/stock-inventaire.png)

Après le décompte physique des stocks, les quantités sont repotrtés dans la colone **_Compté_** de chque article. A la fin l'inventaire, le **Gestionnaire des stocks** le valide et les stocks sont automatiquement mis à jours en cas de différences. 

## Rebuts

Les rebuts sont des produits décomptés dans les stocks mais inutilisables pour un quelconque cause. Pour les défalquer des stocks il faut créer un nouveau **_Rebuts_** et renseigner l'article concerné et la quantité à défalquer. Une le que **Rebut** est validé par le **Gestionnaire des stocks** les quantités des articles disponibles sont automatiquement mises à jours. 

# Analyse 

La partie analyse permet aux **Gestionnaires des stocks** de visualiser des vues synthétiques de la situation des stocks sous différentes formes : listes, tableau croisé, graphes.

![](./images/stock-analyse.png)

# Vue d'ensemble 

La partie vue d'ensemble est un tableau de bord permettant de visualiser en temps réel l'état des différentes opérations selon leur types.

![](./images/stock-vue-ensemble.png)


# Plus de détails 

- Pour la collaboration sur les formulaires de ce module, consulter la fonctionnalité [conversations](./odoo-conversations.md).
- [Site officiel d'odoo](https://www.odoo.com/fr_FR/page/warehouse).  

----
[Retour au sommaire](./odoo-deploy-guidelines-fr.md)