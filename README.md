# Projet « Bien Tourner »

## Liste des compétences couvertes par le projet

### Développer la partie front-end d’une application web ou web mobile en intégrant les recommandations de sécurité

- [ ] Maquetter une application 
- [ ] Réaliser une interface utilisateur web statique et adaptable 
- [ ] Développer une interface utilisateur web dynamique
- [X] Réaliser une interface utilisateur avec une solution de gestion de contenu ou e-commerce

### Développer la partie back-end d’une application web ou web mobile en intégrant les recommandations de sécurité

- [ ] Créer une base de données 
- [ ] Développer les composants d’accès aux données
- [ ] Développer la partie back-end d’une application web ou web mobile 
- [X] Élaborer et mettre en oeuvre des composants dans une application de gestion de contenu ou e-commerce


## Résumé du projet

J’ai effectué un stage de fin de formation du 04/11/2020 au 08/01/2021 au sein de l’Agence de communication « Bien Encré ». Compte tenu du contexte sanitaire, le stage s’est fait en distanciel. Les échanges se faisaient par visioconférence, mail et conversation téléphoniques. Les livrables ont été présentés en présentiel. Le gérant et maître de stage a exprimé le besoin de mettre en place un outil permettant d’interagir avec les téléspectateurs de son émission sportive sur le web tv « dijon-sportnews.fr ». En parallèle, l’outil était destiné à couvrir ponctuellement une émission de téléthon de Décembre 2020. 

L’outil devait intégrer un compte administrateur capable de créer et gérer des comptes utilisateurs, un chat, un sondage, la possibilité de passer en webcam et la diffusion de vidéo en directe. L’outil doit être adapté à la charte graphique. Notre maître de stage nous a demandé d’identifier une solution existante, de la paramétrer et de la personnaliser, puis de la déployer.

Notre choix s’est porté sur le système de visio-conférence Bigbluebutton. C’est un logiciel libre, très bien documenté, paramétrable et déployable en suivant une procédure d’installation sur un serveur. Cette solution intègre toutes les fonctionnalités attendues par le commanditaire.
Nous avons mené des recherches sur le serveur à utiliser. L’outil devait permettre d’accueillir une centaine de personnes.  Mais pour anticiper un développement éventuel des activités, un serveur dédié chez le fournisseur OVH a été mis en place.  Nous y avons installé linux comme noyau du système d’exploitation avec une distribution Ubuntu Server. Nous avons installé Bigbluebutton via le protocole SSH sur un serveur distant. Pour la gestion de la sécurité, l’installation ne peut se faire que sur un nom de domaine avec un certificat SSL.
L’affichage du back-office est géré par la surcouche Greenlight que nous avons installée à la place de l’API démo de Bigbluebutton. Pour le salon de visio-conférence à proprement parler, l’affichage est géré par HTML5 client. Nous avons personnalisé l’outil afin de l’adapter à la charte graphique. Nous avons par la suite effectué des tests de fonctionnalités. 

En finalité nous avons pu livrer un outil fonctionnel répondant à l’attente du commanditaire. Toutefois, ce projet ne couvrant pas la totalité des champs du référetiel, j'ai décidé de présenter un second projet réalisé en cours de formation. 


## Cahier des charges

### Expression des besoins

- **Objectif :** Créer un outil de *live* interactif pour les évènements (émissions *web tv*). 
- **Prise en compte de l'existant :** diffusion via Facebook Live ou Youtube Live d'émissions sportives tournées dans les locaux de l'agence Bien Encrée. 
- **Problématiques :** 
    - besoin d'un service autonome, indépendant des grandes marques que sont Facebook et Youtube, auto-hébergé et reprenant l'identité de l'entreprise Bien Encré et de la marque Bien Tourné ;
    - besoin de pouvoir offrir aux spectateurs la possibilité d'interragir, de communiquer dans un espace privé, géré par un prestataire de confiance - la société Bien Encré - pour ce qui est de l'utilisation des données personnelles collectées, etc. plutôt que de passer par des services grands publics hébergés en Californie et dont on ne maîtrise pas les politiques de confidentialité relevant d'un Droit différent du Droit Français.
- **Fonctionnalités attendues :** 
    - *Partie publique :*
        - pouvoir diffuser du contenu vidéo à partir de liens Youtube ou Facebook ;
        - fonctionnalité de sondage en temps réel ;
        - système de messagerie instantanée ;
    - *Partie Administration :*
        - un compte administrateur pour gérer de comptes utilisateurs ;
        - des comptes utilisateurs ;
- **Livrable attendu et critère d'évaluation de la réussite du projet :** un service fonctionnel, déployé sur un serveur de production et utilisé pour diffuser des *lives* interractifs. 
- **Publics cibles :** 
    - les spectateurs historiques de l'émission, 
    - d'éventuels nouveaux spectateurs rassurés par les problématiques solutionnées par le nouveau service proposé suite à la communication sur la mise en place de ce service.
- **Ressources humaines allouées à la conception et à la réalisation du projet :**
    - Pilotage du projet : Thomas Hazebrouck, dirigeant de l'agence Bien Encré ;
    - Conception et réalisation : Dimitri Hoerth, Adeline Levionnois, Marius Paquet, Tsiry Rafanoharantsoa, stagiaires ;
- **Ressources matérielles allouées :** un serveur dédidé, loué chez OVH, offre infra 2 : 64Mo / 2*1 To SSD / 2*3ToHDD ;

> Remarque : le choix de la solution d’hébergement s'est porté sur OVH car les serveurs proposés par IONOS ne supportent pas Ubuntu 16.04 qui est nécessaire pour faire tourner « Bigbluebutton », la solution identifiée.

### Cadre temporel
- **Du 04/11/2020 au 10/11/2020, phase d'initialisation et de lancement du projet :** recueil du besoin, identification de solutions pour solutionner les problématiques soumises à l'équipe technique, proposition de solution (la technologie GreenLight et la solution BigBlueButton) pour validation ;
- **Du 12/11/2021 au 27/11/2021, phase de conception et de développement :** location du serveur, installation du système d'exploitation (noyeau Linux, distribution Ubuntu 16.04 Xenial Xerus LTS, serveur NGINX) et déploiement puis configuration de la solution BigBlueButton ;
- **Du 27/11/2020 au 24/12/2021, phase de déploiement et de tests :** Personnalisation du service, phases de tests, recueil des retours utilisateurs, solutionnement de la problématique du déploiement du système de gestion de contenu WordPress qui nécessite l'utilisation d'un serveur web Apache dans son utilisation la plus courante, et qu'il fallait déployer sur NGINX ;
- **Du 04/01/2021 au 08/01/2021, phase livraison et de fonctionnement :** 
    - **06/01/2021 :** livraison du produit fini.

### Spécifications fonctionnelles



## Spécifications techniques du projet

## Réalisations

## Présentation du jeu d’essai 

## Veille sur les vulnérabilités de sécurité

## Recherche à partir de site anglophone

## Extrait du site anglophone


# Projet « Portfolio »
 
## Liste des compétences couvertes par le projet

## Résumé du projet

## Spécifications fonctionnelles du projet

## Spécifications techniques du projet

## Réalisations

## Présentation du jeu d’essai 

## Veille sur les vulnérabilités de sécurité

## Recherche à partir de site anglophone

## Extrait du site anglophone