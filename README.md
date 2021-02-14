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

![Logo Bien-tourné](https://i.ibb.co/2yYw3mq/logo.jpg)

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

Tout au long de ma formation et de mon stage en entreprise, j'ai effectué une veille régulière, principalement sur le réseau social professionnel LinkedIn. J'ai commencé par suivre des stagiaires de ma formation en développement web, puis j'ai élargis mon réseau à des professionnels du secteur, au niveau local, régionnal, national puis internationnal. J'ai pu me tenir informé de l'actualité de la discipline que j'étudie en suivant les bonnes personnes, qui communiquent sur les résultats de leur veille informationnelle, qui relaient ou publient des articles. Je me suis moi-même habitué à interragir avec des publications, en manifestant mon intérêt par des « J'aime ». Ce faisant, je pense avoir nourri l'algorithme de LinkedIn sur mes centres d'intérêts, j'ai en tous cas constaté que les propositions de publications dans mon fil d'actualité s'affinaient en terme de pertinence au fur-et-à-mesure de mon utilisation. 

J'ai aussi utilisé la fonctionnalité « Actualités » du moteur de recherche Google combiné à des filtres de date et de pertinence pour identifier moi-même des articles pertinents à re-partager. Pour ce faire, j'ai utilisé des mots-clés généralistes comme « web design », « développement web », « programmation informatique », « cyber-sécurité » ou plus spécialisé, notamment des noms de technologie. 

De plus, je me suis intéressé aux différentes sources d'information issues de la presse spécialisée, que ce soit les versions numériques de journaux papiers ou des blogs. Je consulte en effet régulièrement le site web « programmez.com » ainsi que « BDM - le blog du modérateur », ou « awwwwards », qui met en avant les sites web les plus spectaculaires en terme de conception graphique.

Depuis que je suis un veilleur actif, les problématiques de sécurité informatique ont particulièrement retenue mon attention, les publications sur ce sujet sont nombreuses. 

Durant mon stage, un article du magazine « Programmez! » m'a marqué, il s'intitule « Deviner un mot de passe en observant les épaules de celui qui le saisit » et peut être consulté à l'adresse suivante : https://www.programmez.com/actualites/deviner-un-mot-de-passe-en-observant-les-epaules-de-celui-qui-le-saisit-31154 et se réfère lui-même à l'article datant du 22 octobre 2020 intitulé « Zoom on the Keystrokes: Exploiting Video Calls for Keystroke Inference Attacks » par Anindya Maiti, et publié dans la catégorie « Cryptography and Security » sur le site de l'Université Cornell (Ithaca, New York) qui peut être consulté à cette adresse : « https://arxiv.org/abs/2010.12078 »

Ces articles traitent de la technique de piratage qu'on nomme «  attaque par inférence de frappe ».

> « Une attaque par inférence de frappe désigne toute méthode qui déduit ce qu'un utilisateur est en train de taper via un canal latéral, c'est-à-dire autrement qu'en regardant les mains et les doigts sur le clavier. »

L'attaque par inférence de frappe consiste donc à deviner les touches sur lesquels quelqu'un que l'on regarde via un système de visio-conférence a pu taper lorsqu'il écrit des informations sensibles, par exemple un mot de passe, en regardant non pas les doigts qui ne sont pas dans le champs de la *webcam* mais les épaules. 

> « Mais là où ça devient un peu un scénario à la James Bond, c'est qu'il n'est pas nécessaire que le webcam montre les mains de la personne attaquée. Il suffit qu'elle montre ses épaules pour qu'il soit possible de déterminer ce qu'elle frappe sur son clavier.  »

Ce sujet est particulièrement intéressant pour des développeurs qui doivent déployer un système de visio-conférence à destination du grand public. En effet, il est tout à fait envisageable que les utilisateurs de notre système de visio-conférence basé sur la solution « BigBlueButton » suivent les *lives* sportifs depuis un PC, et laissent à certain moment la plateforme tournée en tâche de fond tout en continuant à surfer sur internet. Si leur *webcam* reste active à ce moment, ils sont extrêmement vulnérables à de potentiels autres spectateurs maîtrisant la technique de l'attaque par inférence de frappe. Mais comment cela fonctionne-t-il ? 

> « Dans le cas de l'analyse des épaules, les chercheurs s'appuient sur un principe élémentaire de la mécanique newtonienne : quel que soit votre style de frappe personnel, lorsque vous appuyez sur une touche, une «force de réaction» dans la direction opposée est produite.
>
> Cette force se déplace ensuite des doigts sur le clavier jusqu'aux muscles et aux articulations de l'épaule, qui l'absorbent. Cette force crée des mouvements petits et subtils, mais mesurables, des épaules, explique les chercheurs, qui précisent que parce que chaque doigt est relié différemment des autres au poignet, la force de réaction d'une frappe se propage légèrement différemment à travers les muscles et les articulations des bras et des épaules, en fonction du doigt utilisé pour appuyer sur la touche... »

Si la précision de cette technique est de 75% en laboratoire, elle ne permet de deviner des mots de passe que dans 25% des cas en condition réelle, notamment parce que les conditions de perception varient (luminosité, position de la caméra, etc.). Mais l'article finit sur le risque de combinaison de cette technique avec d'autres.

La question qui se pose lorsqu'on est sensibilisé à cette problématique, c'est évidemment : « quelles solutions possibles ? ». Or, les études portent sur l'utilisation d'un système de visio-conférence bien précis et très utilisé et répandu : Zoom. On peut évidemment envisager que la technique puisse facilement s'étendre aux autres systèmes de visio-conférence, toutefois j'ai été attentif à cette période aux critiques apportés à l'encontre de Zoom, notamment parce que d'autres critiques, plus directement liées à des problématiques techniques, ont émergé sur la sécurité de cette application depuis le début de la crise du coronavirus. 

J'ai notamment repéré un article intéressant datant du 03/11/2020 intitulé « Visioconférence : les alternatives à Zoom et Teams » et qui cite dès la première ligne la solution BigBlueButton que nous avons identifié pour répondre aux besoins exprimés et que nous avons proposé comme solution de visio-conférence puis qui a été retenu dans le cadre de notre stage. L'article en question peut être consulté à cette adresse : https://www.voyages-d-affaires.com/visioconference-alternatives-zoom-teams-20201103.html



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

##### Mes compétences

La partie « Mes compétences » établit comme son nom l'indique la liste des choses que je sais faire. J'ai décidé de la placer avant les *cards* présentant les projets pour produire une sorte de *teasing* : l'attraction forte du portfolio, ce sont évidemment les projets, c'est ce que les visiteurs vont chercher. Dans une logique UX, pour les contraindre à voir le reste du contenu (ou tout au moins à le survoler si ils utilisent le lien dans la barre de navigation, grâce à un effet *smooth scroll* en CSS), mes réalisations n'apparaissent que dans un troisième temps. De plus, la partie concernant mes projets dirige vers des sites externes à mon portfolio, d'où l'importance de ne pas immédiatement prendre le risque de voir le visiteur quitter le portfolio et potentiellement ne pas y revenir.

##### Mon parcours

Cette partie du *One Page* se divise en trois sous-partie, alignées horizontalement sur un écran de taille moyennes :
- Mes technologies 
- Mes formations
- Mes expériences 

##### Réalisations

Présentation classique sous forme de *cards*, connectée à la base de données alimentée par le *back-office*, je liste mes projets, récupère leur titre, l'image mise-en-avant, la description et les technologies utilisées, ainsi que les liens matérialisés sous forme d'icônes.

Un système de filtres en JavaScript permet de trier les projets. Par défaut, tous les projets s'affichent. On peut filter les projets selon les critères « Conception graphique », « Développement Web » et « Gestion de projet ».  


##### Contacts

La partie « contact » est composée d'un formulaire en PHP qui redirige les informations renseignées par les utilisateurs sur mon adresse mail. Il n'y a pas d'insertions de données dans la base de données sur cette fonctionnalité.

##### Le Footer

Le *footer* se compose de deux lignes : 
- une partie liens vers mes réseaux sociaux sous forme d'icônes ;
- une ligne contenant le nom de l'auteur, en l'occurence moi, et un lien vers la page « Mention Légale ». Dans une précédente version, j'avais commis l'erreur de mettre le logo « *copyright* » qu'on voit couramment, par mimétisme et manque de compréhension de ce que cela impliquait. Le « *copyright* » relève en fait du droit américain et n'a aucune valeur juridique en France.

## Spécifications techniques du projet

### Développement *back-end*

#### Présentation de la solution

Pour répondre à l'objectif de présentation de mes travaux en *Web Design* et en *Web Development*, j'ai choisi de créer un site *one page* personnalisé en *flat design* avec des couleurs rassurantes et de tendances. En plus d'un bon visuel, l'interface visiteur est connecté à une base de donnée et affiche son contenu en dynamique. Pour confirmer par la pratique les technologies citées dans les compétences, j'ai proposé de créer un *back-office* que j'ai développé *from scratch* en PHP/MySQL et qui gèrer l'ajout, l'affichage, la modification et suppression (*CRUD*) ;

#### Choix technologiques

J'ai choisi les technologies en fonction de mon niveau d'expertise sur les technologies mais aussi en considérant la dimension personnel du projet. 

##### Technologie de gestion du projet

**Git**

J'ai utilisé cet outil pour versionner mon code au fur et à mesure des avancées du projet. De cette manière, je pouvais me repositionner sur une version antérieur dans le cas d'une perte accindentèle du code. C'est un outil de développement sécurisant et indispensable 

**Github**

J'ai utilisé cette plateforme collaborative pour poster le projet dans un but principalement de partage. Etant donné que je menais le projet en individuel, je n'ai pas eu à utiliser et à gérer les problématiques des *merge* lors des *pull* et *push* comme ça avais été le cas sur d'autres projets de groupe en formation. Néanmoins, j'ai créé un repository du projet dans lequel je faisais régulièrement des *push*. J'ai créé une petite déscription du projet sur le *repository* et fais en sorte que les commentaires de mes *commit* soient les plus représentatifs des fonctionnalités ou des étapes franchies.

##### Technologie de développement utilisé 

j'ai structuré le code de manière classique sans utilisé une bibliothèque de *pattern Model View Controller*. Le projet n'étant pas d'envergure. Un code bien organisé et bien structuré suffisait amplement même pour l'entretien du site en phase d'exploitation. Mais dans une logique d'amélioration, cela constituerais la prochaine étape du projet.

**Intégration avec HTML, Boostrap et CSS**

Pour le *back-office*, les  pages web sont intégrés en HTML. Bootstrap 5 est utilisé pour gérer la responsivité, il intègre une librairie CSS.  Contrairement à ces précédentes versions pour gérer le dynamisme de l'interface, la version 5 n'utilise plus *JQUERY* au profit de code pur *Javascript*. J'ai modifié le CSS de Bootstrap à plusieurs niveau du site.

**MYSQL**

La partie interaction avec la base de donnée est gérée avec des requêtes SQL. Je me connecte à ma base en locale dans PHPMYADMIN par le protocole PDO de MySQL. J'ai opté pour ce mode de connexion pour faciliter la migration de la base sur un autre gestionnaire tel que Oracle si le besoin se présente, contrairement au protocole *mysqli* qui est propre à MySQL.

**MySQL Workbench**

Pour formaliser le Modèle Conceptuel de Données, le Modèle Logique de Données et le Modèle Physique de Données. J'ai utilisé MySQL Workbench.

**PHP**

Je combine les requêtes SQL avec des boucles et des conditions PHP pour gérer le transfert des informations entre les pages et le traitement des données dans la base. Par souci de sécurité, à chaque formulaire remplie, je néttoie les données fournies avec les fonctions *strip_tags* pour nettoyer les informations renseignées de balises script ou autres injectées par des utilisateurs maladroits, *prepare* pour la préparation de la reqûete et *bindValue* pour accrocher les paramètres lors de l'insertion en base.

De la même manière je gère la récupération des données lors de l'affichage, mes requêtes sont enveloppées dans du SQL mais sans la partie sécurité.

#### Conception de la base de données 

##### Structure de la base de données

Cette base de données se compose de 2 tables. Les tables « utilisateurs » et « projets » sont liées : lorsqu'un utilisateur crée un projet, ce projet lui est attribué, il y a donc une relation : la clé primaire de l'utilisateur est affectée comme clé secondaire au projet. 

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

