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

- **Enjeux et objectifs :** Créer un outil de *live* interactif pour les évènements (émissions *web tv*). 
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
- ***Benchmark :***
    - Youtube Live ;
    - Facebook Live ;
    - Twitch ;
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
- **Du 04/01/2021 au 08/01/2021, phase de production et d'exploitation :** 
    - **06/01/2021 :** livraison du produit fini.

### Conception graphique

#### Logo

#### Charte graphique

#### UI KIT

### Stratégie *marketing*

#### Extrait du *benchmark*

##### Youtube Live

![Interface d'accueil de Youtube Live](https://i.ibb.co/T1dbgSZ/youtube-live.jpg)
![Interface d'un Live](https://i.ibb.co/pWmQWrV/youtube-live2.jpg)

- Analyse *SWOT* : 
    - Forces : le service est connu et identifié par tout le monde, l'interface est ergonomique ;
    - Faiblesses : surchargé, généraliste, faible transparence sur ce qu'il advient des données recueillies ;
    - Opportunités : produire un service spécialisé qui cible un public qui connait et a confiance dans le prestataire de ce service ;
    - Menaces : des moyens collossaux sont attribués pour le développement, la maintenance, les évolutions et l'optimisations des services proposés.

##### Facebook Live

##### Twitch

#### Périmètre fonctionnel et *impact mapping*

![impact mapping du site bien tourné](https://i.ibb.co/2qGfBqT/impact-mapping.jpg></a>)

### Spécifications fonctionnelles

#### Arborescence de l'application
L'application permet de créer d'accéder à l'espace d'administration. Il y a plusieurs profils d'utilisateur de l'espace d'administration avec des droits différents.

![Screens de l'interface](https://i.ibb.co/J7z6Tb5/1.jpg)

![Screens de l'interface](https://i.ibb.co/R9ZY8C6/2.jpg)

![Screens de l'interface](https://i.ibb.co/28jCk7v/3.jpg)

![Screens de l'interface](https://i.ibb.co/NW9P639/4.jpg)

![Screens de l'interface](https://i.ibb.co/ZJkgxg2/5.jpg)

![Screens de l'interface](https://i.ibb.co/jzwLVN9/6.jpg)


## Spécifications techniques du projet

## Réalisations



## Présentation du jeu d’essai 

## Veille sur les vulnérabilités de sécurité

## Recherche à partir de site anglophone

## Extrait du site anglophone


# Projet « Portfolio »
 
## Liste des compétences couvertes par le projet

### Développer la partie front-end d’une application web ou web mobile en intégrant les recommandations de sécurité

- [X] Maquetter une application 
- [X] Réaliser une interface utilisateur web statique et adaptable 
- [X] Développer une interface utilisateur web dynamique
- [ ] Réaliser une interface utilisateur avec une solution de gestion de contenu ou e-commerce

### Développer la partie back-end d’une application web ou web mobile en intégrant les recommandations de sécurité

- [X] Créer une base de données 
- [X] Développer les composants d’accès aux données
- [X] Développer la partie back-end d’une application web ou web mobile 
- [ ] Élaborer et mettre en oeuvre des composants dans une application de gestion de contenu ou e-commerce

## Résumé du projet

Dans le cadre de ma formation Access Code School, j'ai développé un portfolio pour présenter mes travaux en *Web Design* et en *Web Development*. 

L'objectif de ce projet était de proposer une solution complète, développée avec des technologies *front-end* (HTML / CSS / JS et le *framework* Bootstrap) et des technologies *back-end* (PHP et MySQL).

Cette solution est composée : 
- d'une interface visiteur, récupérant dynamiquement du contenu à afficher dans une base de données ; 
- d'un *back-office* que j'ai développé *from scratch* en PHP/MySQL pour ajouter, afficher, modifier et supprimer (*CRUD*) ;

## Cahier des charges

### Conception graphique 

#### *Benchmark*

#### Charte graphique

##### Palette chromatique

##### Typographies

##### UI KIT

#### Maquettes

### Spécifications fonctionnelles du projet

#### Développement de l'interface du *back-office*

##### La page de connexion

Il s'agît de la page « index.php ». Elle se compose d'un formulaire de connexion permettant de renseigner un nom d'utilisateur et un mot de passe. Le script vérifie si ce nom d'utilisateur et ce mot de passe sont enregistrés dans la base de données, si c'est le cas, on accède à la page « home.php ». Dans le cas contraire, on reste sur cette page, qui propose aussi un lien vers la page « register.php » permettant de soumettre une demande d'inscription.

##### La page d'inscription d'un nouvel utilisateur

Il s'agît de la page « register.php » Elle permet de soumettre une demande d'inscription via un formulaire. Le visiteur doit renseigner un nom d'utilisateur, un email et un mot de passe, qu'il doit re-taper par sécurité dans un second champs de type *password*.

Lorsqu'un utilisateur soumet une inscription, le programme vérifie la correspondance des deux mots de passe saisie puis crypte le mot de passe avant de l'insérer dans la base de données.

##### La page listant les projets

Il s'agît de la page « home.php ». Cette page se connecte à la base de données et affiche le titre de tous les projets contenus dans la table « projects », ainsi que leurs technologies. 

En cliquant sur l'icone représentant une page web, on accède à la page « details.php » pour consultation des informations enregistrées en base de données concernant le projet sélectionné.

Un bouton « ajouter un projet » permet d'accéder à la page « add.php ». 

Depuis cette page, on peut aussi modifier ou supprimer un projet existant et changer sa visibilité, ou encore se déconnecter du *back-office*.

> La requête pour récupérer les informations affichées sur cette page est la même que celle utilisée sur la page listant les projets de l'interface visiteur du portfolio. 

##### La page de création d'un projet

Il s'agît de la page « add.php ». C'est un formulaire permettant de renseigner toutes les informations concernant un nouveau projet : son titre, sa période de réalisation, se technologies, la description du projet, sa visibilité par défaut (masquée ou affichée), son image mise-en-avant, et les liens vers le projet en ligne, les maquettes *desktop* et *mobile* et son github.

##### La page affichant un projet

Il s'agît de la page « details.php ». Elle affiche toutes les informations concernant un projet en fonction de son id. Une icône indique la possibilité de modifier les informations, elle redirige sur la page « edit.php ». Une autre icône permete de naviguer vers la page listant les projets.

##### La page de modification d'un projet

Il s'agît de la page « edit.php ». Elle affiche un formulaire reprenant les informations concernant un projet en fonction de son id.

Elle permet aussi de charger une nouvelle image qui remplace l'image existante.

#### Développement *front-end*

L'objectif de la partie visiteur de mon portfolio de développeur web est de permettre à des personnes s'intéressant à mon profil en vue d'un éventuel recrutement d'en savoir plus sur mes compétences et de découvrir les projets sur lesquels j'ai travaillé. Mon portfolio est donc un site de type *One Page* composé de cinq ancres :
- Accueil ;
- Mes compétences ;
- Mon parcours ;
- Réalisations ;
- Contacts ;

##### L'accueil 

La première information qui doit sauter aux yeux du visiteur est que je suis un *designer* et developpeur web. C'est donc l'information centrale de la rubrique Accueil, qui se compose aussi du menu et d'une photo animée afin de se familiariser avec moi. 

Pour mieux comprendre mon identité, j'ai cherché à mettre en avant mes origines, ce qui explique le logo de mon portfolio : une image au format vectoriel représentant Madagascar, mon pays d'origine. J'ai réalisé ce logo avec Adobe Illustrator, j'ai chargé une carte de Madagascar dans un format BITMAP, j'ai utilisé l'outil plume pour faire un tracé des contours puis j'ai utilisé l'outil concepteur de forme pour obtenir la version vectorisée, j'ai ensuite travaillé sur les couleurs.


## Spécifications techniques du projet

### Développement *back-end*

#### Conception de la base de données 

##### Structure de la base de données

Cette base de données se compose de 2 tables. Les tables « utilisateurs » et « projets » sont liée : lorsqu'un utilisateur crée un projet, ce projet lui est attribué, il y a donc une relation : la clé primaire de l'utilisateur est affectée comme clé secondaire au projet. 

- la table « users » :
    - id (pk)
    - username
    - email
    - password

- la table « projects » :
    - id (pk)
    - user_id (sk)
    - title
    - technologies
    - description
    - visibility (hide / visible)
    - thumbnail 
    - project_link
    - mobile_mockup_link
    - desktop_mockup_link
    - github_link

##### Modélisation de la base de données

![Capture d'écran de la modélisation de la base de données dans MySQL Workbench](https://i.ibb.co/XzWz6yV/mysql-workbench.jpg)



## Réalisations

## Présentation du jeu d’essai 

## Veille sur les vulnérabilités de sécurité

