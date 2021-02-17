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

#### Charte graphique

![Logo et couleur Bien-tourné](https://i.ibb.co/g3YrStC/charte-graphique-bien-tourenr.png)

#### UI KIT

### Stratégie *marketing*

#### Extrait du *benchmark*

##### Youtube Live
![Interface d'accueil de Youtube Live](https://i.ibb.co/T1dbgSZ/youtube-live.jpg)
![Interface d'un Live](https://i.ibb.co/0tfSBCj/youtubelive.jpg)
![Interface d'un compte](https://i.ibb.co/CW93pZq/compteyoutube.jpg )

##### Facebook Live

![Interface d'un compte](https://i.ibb.co/TvRBPYn/facebooklive.jpg )


- Analyse *SWOT* : 
    - Forces : les services sont connus et identifiés par tout le monde, l'interface est ergonomique ;
    - Faiblesses : surchargé, généraliste, faible transparence sur ce qu'il advient des données recueillies ;
    - Opportunités : produire un service spécialisé qui cible un public qui connait et a confiance dans le prestataire de ce service ;
    - Menaces : des moyens collossaux sont attribués pour le développement, la maintenance, les évolutions et l'optimisations des services proposés.


#### Périmètre fonctionnel et *impact mapping*

![impact mapping du site bien tourné](https://i.ibb.co/2qGfBqT/impact-mapping.jpg></a>)

### Spécifications fonctionnelles
Dans cette partie du projet, nous avons choisies une palette de couleur à utiliser pour l'interface de Greenlight. En effet, un des critères attendus du site c'est la cohérence des couleurs avec le logo de la marque. J'ai créé une petite plateforme graphique composée uniquement des couleurs du logo sans la typographie.


#### Arborescence de l'application
L'application permet d'accéder à l'espace d'administration ou utilisateur selon le profil de connexion. Les droits son gérés par l'administrateur depuis son espace.

![Screens de l'interface](https://i.ibb.co/qmnDN6f/arborescencebientourn.png)

#### Visuel du site
Une des spécificité de ce projet concenant la partie conception, c'est que nous n'avons pas eu à créer une maquette. En effet, la surcouche Greenlight a déjà son propre affichage. Toutefois, il est intéressant de présenter un visuel du site :

![Screens de l'interface](https://i.ibb.co/J7z6Tb5/1.jpg)

![Screens de l'interface](https://i.ibb.co/R9ZY8C6/2.jpg)

![Screens de l'interface](https://i.ibb.co/28jCk7v/3.jpg)

![Screens de l'interface](https://i.ibb.co/NW9P639/4.jpg)

![Screens de l'interface](https://i.ibb.co/ZJkgxg2/5.jpg)

![Screens de l'interface](https://i.ibb.co/jzwLVN9/6.jpg)


## Spécifications techniques du projet

### Choix technologiques

En l'absence d'encadrement technique au sein de la structure d'accueil, il nous fallait identifier un outil à implementer en autonomie. C'est la contrainte la plus importante que nous devions considérées lors de la recherche de solution durant la phase d'initialisation du projet.  Nous avons basé notre choix de l'outil Bigbluebutton sur sa facilité de prise en main grâce à sa documentation très élaborée. 

### Domaine et hébergement

**Solution d'hébergement**

Un serveur dédié *bare metal (métal nu)* chez OVH a été loué pour héberger Bigbluebutton. Nous l'avons doté d'une bonne capacité de stockage (500Go), utile pour les enregistrements des sessions.
Les technologies utilisées par l'application générent d'importants flux de données. Nous avons considérés que les flux audio et vidéos générés lorsque les *webcams* des quelques centaines de personnes sont activés recquiert une importante bande passante si le cas se présentais. Nous avons établi notre bande passante à 1Gbits/s. La configuration minimale recquise du serveur étant fixé à 250Mbits/s.

**Système d'exploitation Linux**

Sur recommandation de la documentation, nous avons mis en place une distribution Ubuntu 16.04 -Xenial xerus -  64 bits exécutant le noyau Linux.

**Protocole utilisé**

Le SSH est le protocole d'installation attitré à Bigbluebutton. Pour le transfert des fichiers, j'ai utilisé le protocole FTP. 

**Serveur Web**

Le serveur Web utilisé par Bigbluebutton est Nginx.

**Gestion de l'affichage**

Greenlight  est une application Ruby on Rails qui fournit une interface simple aux utilisateurs pour créer des salles, démarrer des réunions et gérer les enregistrements. Il intègre un support complet pour la gestion des comptes utilisateurs. Greenlight permet également aux utilisateurs de mettre à jour les informations de leur compte à tout moment (mot de passe, image de profil, etc).

**Gestion de la sécurité**

Pour la sécurité, nous avons ajouter le support SSL à notre serveur BigBlueButton. De plus, sur certaine version de navigateur comme chrome 47, les utilisateurs de Chrome ne peuvent pas partager leur microphone via WebRTC à moins que BigBlueButton ne soit chargé via HTTPS. Pour ce faire, nous avons attribué un nom d'hôte à notre serveur BigBlueButton en l'occurence "Bien-tournér.fr". Un certificat SSL existait déjà sur ce domaine. Nous avions configuré Nginx pour utiliser SSL et afficher du contenu en HTTPS.

Dans cette même logique de sécurité, nous avons désinstallés l'API démos de Bigbluebutton car avec celui ci n'importe qui pouvait accéder sans authentification à notre serveur. Nous avons installé Greenlight qui prends en charge quatre types d'authentification : 

- En application (Greenlight)
- Google OAuth2
- Office365 OAuth2
- LDAP

Tous ces fournisseurs d'authentification sont configurables et peuvent être activés / désactivés individuellement.

### Accéssibilité et adaptabilité

L'outil bigbluebutton est adaptable à tout type d'appareil. Il intègre également des palettes de couleurs accéssibles aux mal voyants. 

## Réalisations

**installation du système d'exploitation**

Après avoir retenue Bigbluebutton comme solution à mettre en place et obtnue l'accès au serveur d'hébergement, j'ai commencé par l'installation du système d'exploitation du serveur avec mon collègue Marius Paquet. OVH intègre un service d'installation automatique. Nous avons eu recours à cette procédure. Pour cela, j'ai paramétré l'installation avant de la lancée. J'ai effectuée les actions ci dessous : 

- Cliquer sur les trois points dans la partie "Système OS (Non installé)" puis choisir le noyau et la distribution souhaité  :

![Procédure d'installation de l'OS](https://i.ibb.co/KNXK7ws/boutoninstall.png)


- Choisir un template d’installation OVH pour accéder à l’installation automatique des systèmes d'exploitation supportés par le serveur dédié et cliquer sur suivant :

![Procédure d'installation de l'OS](https://i.ibb.co/PGrRssp/choixtemplatesdinstallation.png)

![Procédure d'installation de l'OS](https://i.ibb.co/G9gvmFD/choixOS.png)

![Procédure d'installation de l'OS](https://i.ibb.co/NWjNCqp/noyaulinux.png)

Nous avons lancé l'installation une fois le paramétrage términé. La deuxième illustration ci-dessous informe sur le système d'exploitation installé avec toutes ses caractéristiques.

![Procédure d'installation de l'OS](https://i.ibb.co/3fC9Sts/runinstallovh.png)
![Procédure d'installation de l'OS](https://i.ibb.co/DMpP3j2/endinstall-OS.png)


**Redirection du nom de domaine vers le serveur**

Le domaine bien-tourné.fr existait déjà et était dirigé sur un serveur mutualisé de l'Agence. Dans l'espace administrateur du serveur mutualisé et dans celui du sereur dédié, j'ai fait la redirection  du domaine vers le serveur dédié pour le faire pointer sur Bigbluebutton.

**Installation de l'application Bigbluebutton**

Comme précisé plutôt, l'installation se fait par le protocole SSH. A la fin de l'installation du système d'exploitation, nous avons reçu un mail de confirmation et les accès au serveur. Il y a trois type d'installation possible de l'outil, une procédure qui s'appelle bbb-instal.sh qui est une configuration rapide, une autre dénommé Ansible pour les déploiements à grande échelle et la dernière l'étape par étape. Nous avons utilisé la procédure bbb-instal.sh qui est un script shell automatisant l'installation pas à pas. Les conditions de réussites son les même pour les trois c'est à dire : obtenir un serveur dédié, s'assurer que le serveur répond aux exigences minimales de BigBlueButton, attribuer un nom d'hôte (recommandé pour configurer SSL) et configurer le pare-feu du serveur (si nécessaire). 

Avant l'installation, nous avons effectuée une série de vérification obligatoire. 

- Vérification des paramètres régionaux du serveur si ils sont en_US.UTF-8 par les commandes ci dessous avec les résultats obtenus: 

        $ cat /etc/default/locale
        LANG="en_US.UTF-8"
        $ sudo systemctl show-environment
        LANG=en_US.UTF-8
        PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin

- Vérification de la quantité de mémoire minimale de 4Go reccquise en lancant la commande $ free -h
 
- Vérification de la distribution Ubuntu 16.04 

        $  cat /etc/lsb-release
        DISTRIB_ID=Ubuntu
        DISTRIB_RELEASE=16.04
        DISTRIB_CODENAME=xenial
        DISTRIB_DESCRIPTION="Ubuntu 16.04.x LTS"

- Vérification de la prise en charge des adresses Ipv6 :

        $ ip addr | grep inet6
        inet6 ::1/128 scope host
        ...

- Vérification de la version du noyau Linux, la version requise est la 4: 

        $ uname -r
        4.15.0-38-generic

- Vérification du processeur du serveur  à 4 cœurs au moins :

        $ cat /proc/cpuinfo | awk '/^processor/{print $3}' | wc -l
        4

Au même titre que les vérifications ci dessus, une mise à jour du serveur est obligatoire pour qu'il soit à niveaur sur les derniers packages et mises à jour de sécurité. Avant cela, quelques petites vérification devaient être effectué sur le serveur lui même. Grosso modo, la commande que j'ai lancé pour la mise à niveau du serveur est :

        $ sudo apt-get update
        $ sudo apt-get dist-upgrade

La signature numérique des packages pour BigBlueButton sont faite avec la clé publique du projet. Il était nécessaire de rajouter à la châine de clés du serveur la clé publique du projet.

        $ wget https://ubuntu.bigbluebutton.org/repo/bigbluebutton.asc -O- | sudo apt-key add - 

En finalité, nous avons lancé le script shell bbb-install.sh qui démarre le processus d'installation de Bigbluebutton. Cette commande est la suivante : 

        wget -qO- https://ubuntu.bigbluebutton.org/bbb-install.sh | bash -s -- -w -a -v xenial-22 -s bbb.example.com -e info@example.com



**Erreur 500**

Au moment du premier test de connexion à une salle de réunion sur l'API démo, l'application qui gère la création et l'accès aux salons, nous avons rencontrée une erreur 500. Le problème vennais de l'adresse IP, il ne correspondait pas au nom d'hote. J'ai donc lancé la commande bbb-conf --setip <adresse IP du serveur> pour résoudre le problème.

![Procédure d'installation de l'OS](https://i.ibb.co/72ZGCfg/setipbbb.png)

**installation de Greenlight**

Une fois le problème de l'adresse IP qui ne résout pas sur le nom d'hôte résolu, j'ai désinstallé l'API démo pour le remplacer par Greenlight, une plateforme qui présente les meilleures pratiques d'utilisation de l'API BigBlueButton. Il est fortement recommandé d'utiliser Docker lors de l'installation de Greenlight sur un serveur BigBlueButton. La procédure consiste à lancer les commandes suivantes : 

        docker -v
        mkdir ~/greenlight && cd ~/greenlight
        docker run --rm bigbluebutton/greenlight:v2 bundle exec rake secret


Grosso modo, la première commande vérifie si docker existe sinon, engager une autre procédure pour l'installer. Puis vient la création du repértoire *greenlight* pour la configuration. La dernière génère le fichier de configuration .env et installe Greenlight qui est enveloppée dans une image de Docker. Greenlight a besoin d'une clé secrète pour fonctionner en production. J'ai lancé la commande ci dessous pour la générée et pouvoir définir sur cette clé le *SECRET_KEY_BASE* dans le fichier .env : 

        docker run --rm bigbluebutton/greenlight:v2 bundle exec rake secret

Par défaut, Greenlight est installer dans un sous /b du serveur. Nous avons gardé cette configuration pour éviter les conflits avec d'autres composants du serveur. 

## Présentation du jeu d’essai 

J'essai de me connecté à mon compte utilisateur pour tester si la connexion se fait. Je renseigne le nom de domaine https://bien-tourner;fr/b.J'arrive bien sur la page d'acceuil de Greenlight. Je clique sur le bouton connexion et j'arrive à la au formulaire de connexion. Je renseigne le mail de mon compte utilisateur et mon mot de passe puis je clique sur connxeion. La connexion est faite, je vois que je suis sur la page de mon compte utilisateur. 

J'essai de créer un salon en cliquant sur le bouton "créer un salon". Une fenêtre modale affiche un formulaire avec une case pour remplir le nom du salon et une liste de paramètres à configurer. Je renseigne le nom TEST et clique sur le paramètre "mettre les utilisateurs en sourdine lors de la connexion". Je clique sur "créer", je suis renvoyé vers la page accueil de mon compte utilisateur. Je vérifie que le salon et lien à envoyer aux personnes invitées ont bien été créés . 

Je test à présent le démarrage d'une session. Je séléctionne un salon puis je clique sur le bouton de "démmarer". Un message me demande de rejoindre l'audio ou de rester en écoute seule. Je choisi de rester en écoute seule. Je clique sur l'icone "casque audio". Un message s'affiche me dit que j'ai rejoint la conférence audio.

J'essai maintenant le partage de vidéo externe. Je récupère un lien d'une vidéo diffusée en direct sur Youtube. Je clique sur le bouton "plus" pour afficher l'option " partager une vidéo externe". Une fenêtre modale s'affiche me demandant d'ajouter l'URL d'une vidéo. Je clique sur "partager une nouvelle vidéo", la vidéo se lance. 

![Procédure d'installation de l'OS](https://i.ibb.co/RQjSSWG/jeud-essai.jpg)


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

J'ai notamment repéré un article intéressant datant du 03/11/2020 intitulé « Visioconférence : les alternatives à Zoom et Teams » et qui cite dès la première ligne la solution BigBlueButton que nous avons identifié pour répondre aux besoins exprimés et que nous avons proposé comme solution de visio-conférence puis qui a été retenu dans le cadre de notre stage. L'article en question peut être consulté à cette adresse: https://www.voyages-d-affaires.com/visioconference-alternatives-zoom-teams-20201103.html



## Description d’une situation de travail ayant nécessité une recherche, effectuée à partir de site anglophone

**Situation de travail** 

Lors de l'installation de notre outil Greenlight, je me suis occupé de créer le compte administrateur. En effet, cette opération ne se fait pas automatiquement mais à initier après déploiment de l'application. Les comptes utilisateurs peuvent être créés par l'administrateur une fois qu'il a son compte ou en passant par le protocole SSH. J'ai effectué les deux types de créations. 

**Recherche effectuée**

Pour ce faire, j'ai donc fait une recherche sur le moteur *Google* en tapant les mots clés "create administrator profil on bigbluebutton". Les résultats affichés par google me redirige en majorité vers la documentation officielle de Bigbluebutton. C'est d'ailleur une des raisons pour lesquelles j'ai utilisé *Google* car c'est le plus précis et le plus rapide. 

![Procédure d'installation de l'OS](https://i.ibb.co/3vxGYdD/rechercheanglophone.jpg)


J'ai pour habitude de vérifier les liens de chaque site pour voir si ils affichent du contenus en Https. Cela me permet de confirmer la fiabilité des informations livrées dans le site. Je vérifie ensuite si le titre et l'extrait du contenu affichés correspondent à ma recherche ou si il manque des mots clés.

C'est ainsi que j'ai pu déduire que le premier lien me redirige vers la documentation officielle de Bigbluebutton, c'est donc bien le lien qu'il me fallait. 

**Consultation et exploitation des informations**

Je procède toujours par un survol des informations de bout en bout, pour confirmer la pertinence des phrases qui contiennent mes mots clés. Ainsi je peux identifier rapidement si ils existent d'autres termes ou mots qui confirme les informations ou mettent la documentation hors cadre.

Dans le cas présent, la documentation confirme bien ce que j'avais besoins. Je me suis connecté au serveur. Et dans le terminal, j'ai lancé la commande de création de compte administrateur suivante : 

    docker exec greenlight-v2 bundle exec rake user:create["name","email","password","admin"]

De la même manière j'ai exécuté la commande de création de compte utilisateur : 

    docker exec greenlight-v2 bundle exec rake user:create["name","email","password","user"]

Il m'a bien retourné l'email et le mot de passe du compte administrateur que j'ai fourni par la suite à mon mâitre de stage et ceux de mon compte utilisateur.


## Extrait du site anglophone


**Creating Accounts**

The following examples assume you have Greenlight installed in the ~/greenlight directory. Before running the commands, change into the ~/greenlight directory.

        cd ~/greenlight

**Creating a User Account**

To create an User account with specified values, in the Greenlight directory, run the following command:

    docker exec greenlight-v2 bundle exec rake user:create["name","email","password","user"]

Once the command has finished it will print the account’s email and password.

**Creating an Administrator Account**

To create an Administrator account with the default values, in the Greenlight directory, run the following command:

        docker exec greenlight-v2 bundle exec rake admin:create

If you would like to configure the name, email, or password of the Administrator account, replace the previous command with this:

    docker exec greenlight-v2 bundle exec rake user:create["name","email","password","admin"]

Once the command has finished it will print the account’s email and password.


**Traduction**

**Créer des comptes utilisateurs** 

Pour les exemples suivants, on suppose que greenlight est déjà installé
dans le repértoire ~/greenlight. Avant de lancer les commandes, accéder au repertoire de greenlight  : 

    cd ~/greenlight

**Créer un compte utilisateur** 

Lancer la commande ci-dessous pour créer un compte utilisateur en spécifiant des valeurs :

    docker exec greenlight-v2 bundle exec rake user:create["name","email","password","user"]

Quand la commande sera prête, elle imprimera  l'email et le mot de passe du compte.

**Créer un compte administrateur**

Lancer la commande ci-dessous dans le repértoire *Greenlight* pour créer un compte administrateur avec les valeurs par défaut :

docker exec greenlight-v2 bundle exec rake admin:create


Remplacer la commande précédente par la suivante si vous souhaitez configurer le nom, l'adresse e-mail ou le mot de passe du compte administrateur :

    docker exec greenlight-v2 bundle exec rake user:create["name","email","password","admin"]

Une fois la commande terminée, elle imprimera l'email et le mot de passe du compte.



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
Avant de me lancer, j'ai effectué une recherche d'inspiration en visitant des sites de portfolio. L'ojectif est d'identifier les tendances du web. J'ai mis en place quelques criètres d'évaluation notamment, l'ergnomie, la typographie, les couleurs. J'ai matérialisé cela par la production d'un *benchmark* dont je présente içi l'extrait : 

![Procédure d'installation de l'OS](https://i.ibb.co/dWGG4NX/Diapositive1.jpg)
![Procédure d'installation de l'OS](https://i.ibb.co/DkyHctT/Diapositive2.jpg)
![Procédure d'installation de l'OS](https://i.ibb.co/WHd53Ct/Diapositive3.jpg)
![Procédure d'installation de l'OS](https://i.ibb.co/QYwQsTY/Diapositive4.jpg)


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

**Back-end**

* Création des tables de la base de données

    Après avoir établi le modèle conceptuel et logique de la base des données, j'ai implementé le modèle physique dans Phpmyadmin en exportant le diagramme que j'ai réalisé dans MySQL Workbench. Cette opération consiste à traduire le modèle conceptuel et logique en un langage de définition de données, en l'occurence celui du SQL. J'ai par la suite copié le code dans l'onglet SQL de Phpmyadmin. J'ai éxécuté le code et Phpmyadmin génére automatiquement mes tables en lisant le code SQL importé.

* Connexion à la base de données

    * J'ai créé une page "db-connect.php" dans laquelle j'établie ma connexion comme suit :

        ![Capture d'écran de la modélisation de la base de données dans MySQL Workbench](https://i.ibb.co/pydHqCG/dbconnect.jpg)

        La première partie de ce code consiste à définir les variables de connexions notamment le nom du serveur, le nom de la base, le nom de l'utilisateur, et un mot de passe. Je crée ensuite une variable $db dans laquelle j'établie une nouvelle connexion avec PDO en identifiant le nom du SGBD, notamment MysQL et les variables de connexions. La dernière partie sert à paramétrer PDO pour qu'il gère les exceptions en cas d'erreurs.

* Connexion au back-office  

    * L'application intègre une page de connexion avec authentification par nom d'utilisateur et mot de passe. J'ai commencé par créer dans ma page index.php un formulaire utilisant la méthode *Post* et qui renvoi les données pour traitement à la page *connexion.php*. Pour la saisie des données, j'ai des *input* de type *text* et *password*. Deux boutons "Se connecter" et "S'inscrire" servent à soumettre les informations renseignés pour traitement dans la page connexion.php ou à rediriger les utilisateurs vers la page *register.php*. J'active une *session_start()* pour passer cette variable  dans connexion.php;

        ![Capture d'écran de la modélisation de la base de données dans MySQL Workbench](https://i.ibb.co/jJKkhpP/index.jpg)
     
    * Dans la page connexion.php, j'effectue le traitement des données récupérées dans la variable *$_POST*  et *$_SESSION*. Avant tout, je me connecte à la base par un *require_once* de ma page *"db_connect.php"*, puis je crée ma requête SQL que j'enveloppe dans une variable. Je prépare ma requête avec *prepare()* avant de l'executé. Cela évite le traitement des scipts injectés par des utilisateurs malveillants. Je traite ensuite la vérification du nom d'utilisateur à un premier niveau puis une seconde vérification, celle du mot  de passe si le nom d'utilisateur est renseigné. 

        ![Capture d'écran de la modélisation de la base de données dans MySQL Workbench](https://i.ibb.co/q1TH9NB/connexion.jpg)


        Si l'authentification réussie, l'utilisateur est redirigé vers la page *home.php", page d'accueil du back-office.

        Inversement, un message d'erreur est affiché si l'authentification a échouée avec une proposition d'inscription. 

        ![Capture d'écran de la modélisation de la base de données dans MySQL Workbench](https://i.ibb.co/ZxHwLTM/errorconnexion.jpg)
  
    * La page register.php est un formulaire gère l'inscription des utilisateurs. ELle utilise également la méthode $_POST et une *session_star()* pour le transfert des données. A ce stade, il est important de renforcer la sécurité des données récupérées dans ce formulaire. Pour gérer cela, j'ai donc mis en place en premier lieu un néttoyage des données par la fonction "strip_tags()" d'écarter les scripts injectés. En second recours, je crypte les mots de passe par un *password_hash*. Puis troisièmement, j'utilise des requêtes préparée par la fonction *prepare()*. Ce qui veut dire que les requêtes sont compilées avant l'insertion des paramètres par la fonction *bindValue()* et l'exécution par la fonction *execute()*. Cette organisation permet d'éviter l'interprétation de codes introduits dans les paramètres. La requête SQL utilisée est *"INSERT INTO"* - *"VALUES"* pour écrire dans la base.  Si des anomalies sont présentes dans les données (champs non renseigné, mot de passe non conforme, mail non conforme), un message d'erreur s'affiche. Et inversement si les données saisie sont correcte, l'utilisateur est redirigé vers la page index.php où la connexion peut être effectuée. Un message de succès s'affiche également.

        ![Capture du code d'inscription](https://i.ibb.co/dL6GrK4/registerrealisationsportfolio.jpg)

    
* Gestion des contenus dans le back-office

    * La page home.php est l'accueil du back-office. C'est une table qui récupère les données existantes dans la table *projects* de la base. J'ai utilisé la condition if ($_SESSION['username']) pour permettre à l'utilisateur connecté de voir la liste des projets. Cette liste est obtenue par une requête SQL *SELECT * FROM \`projects`*

        ![Capture d'écran du code de la page d'accueil](https://i.ibb.co/L82P6RB/home.jpg)

        Pour afficher la liste, j'ai utilisé une boucle PHP *foreach* sur le résultat de la requête SQL. Dans les éléments *td* d'une table j'ai écrit le code PHP qui récupère les valeurs renvoyées par la requete.
        
        ![Capture d'écrand de la boucle de la page d'accueil](https://i.ibb.co/ydnby8S/foreachhome.jpg)
        
        J'ai créé les liens de consultation, modification, visibilité et suppression des projets. Dans les cibles des liens j'ai concatené l'URL et l'identifiant du projet récupéré dynamiquement pour l'envoyer vers chaque page concernée.

        ![Capture d'écran des liens de la page d'accueil](https://i.ibb.co/xL2q00d/homelinks.jpg)

    * J'ai créé formulaire *add.php* pour gérer l'ajout de contenu dans mon back-office. Il reprend les champs de la table *projects*  de la base de données. A la différence des formulaires des pages vue précédements, celui çi gère l'ajout de fichier pour la gestion des images. J'ai donc rajouté  *enctype="multipart/form-data"*. Une div avec la classe *form-file* et un "input" de *"type=file"* sont insérer dans *form*. 
    
        Pour gérer le déplacement des images ajoutées, j'ai définie dans une variable l'emplacement de destination du fichier puis j'ai utilisé la fonction *move_uploaded_file()*.  Le système de gestion de la sécurité par nettoyage des scripts avec strip_tags() et par utilisation d'une requête préparée est repris içi. J'ai utilisé la requête SQL *INSERT INTO* - *VALUES* pour écrire dans la base.
        
        ![Capture d'écran du code page ajout](https://i.ibb.co/1fQXVSR/conditionsadd.jpg)


        ![Capture d'écran du code page ajout image](https://i.ibb.co/vdcHjDK/addimage.jpg)

    * J'ai crée une page *details.php* pour la consultation des projets. Dans cette partie, j'utilise les variables superglobales *$_GET* et *$_SESSION* pour récupérer et traiter l'*ID* contenu dans l'URL afin de séléctionner le projet dans la base. Rappelons que cet état est obtenu par ajout à l'URL de l'*ID* d'un article en cliquant sur l'icone "consulter" dans la page "home.php". La requête utilisée est *"SELECT * FROM"* - *"WHERE"*. Le processus de nettoyage et d'utilisation de requête préparée est de nouveau utilisé.

        ![Capture d'éran de la page de consultation](https://i.ibb.co/GWDZRDL/details.jpg)


    * La page edit.php permet à l'utilisateur de modifier les informations enregistrées dans les champs de la table *projects*. Le principe içi est d'utiliser un formulaire dans lequel les informations existantes dans la base sont prévisualisables et modifiables. Dans le formulaire on execute des requêtes d'affichage des données existantes en donnant comme *"value"* aux *"input"* les valeurs des champs de la table *"projects"*. Le champ "*ID*" doit être dans un élément *input* de type *hidden*.   Cette page est un mixte de la page details.php et add.php. J'ai utilisé les superglobales *$_POST*, *$_GET*, *$_FILE* et *$_SESSION*. 

        ![Capture d'écran de la page de modification](https://i.ibb.co/BTRzdnM/editformpost.jpg)

    
        La première étape consiste à sélectionner par un *$_GET* le projet à modifier pour l'afficher. La deuxième consiste à utiliser un *$_POST* pour récupérer les données du formulaire. J'ai envoyé la valeur de l'*ID* avec les autres informations pour que la modification se fasse précisément sur le projet ayant l'*ID* séléctionné. La requête SQL j'ai utilisé est *"UPDATE"* - *"SET"* - *"WHERE"*.

        ![Capture d'écran de la page de modification](https://i.ibb.co/CvzPrS8/editpost.jpg)

        J'ai traité la modification des images dans un formulaire à part pour éviter que l'image existante dans la base soit écrasée par un tableau vide envoyé dans le formulaire lorsque l'utilisateur ne veut pas modifier l'image mais d'autres informations. 

        ![Capture d'écran de la page de modification](https://i.ibb.co/6JwnBw1/editimg.jpg)

        ![Capture d'écran de la page de modification](https://i.ibb.co/WzrCq15/editimgform.jpg)

    
    * J'ai créé une page delete.php pour pertmettre la suppression des projets. Le principe consiste à sélectionner un projet par son identifian comme avec la superglobale *$_GET*, et une requête SQL *SELECT*  puis d'utiliser une requête *DELETE* - *FROM* - *WHERE* \`id` sans quoi tout sera supprimé.

        ![capture d'écran de la page de suppression](https://i.ibb.co/4shgTpf/delete.jpg)

    * Le principe de la page disconnect.php est de supprimer les variables de la session et la session elle même.

        ![capture d'écran de la page de déconnexion](https://i.ibb.co/hyRnWgd/disconnect.jpg)

**Front - end**

* Connexion à la base de données : 

    * La page "db-connect.php reprend le même script que celui du back-office avec les mêmes principe de gestion des exceptions.
 
         ![Capture d'écran de la modélisation de la base de données dans MySQL Workbench](https://i.ibb.co/pydHqCG/dbconnect.jpg)

        La première partie de ce code consiste à définir les variables de connexions notamment le nom du serveur, le nom de la base, le nom de l'utilisateur, et un mot de passe. Je crée ensuite une variable $db dans laquelle j'établie une nouvelle connexion avec PDO en identifiant le nom du SGBD, notamment MysQL et les variables de connexions. La dernière partie sert à paramétrer PDO pour qu'il gère les exceptions en cas d'erreurs.

* Affichage des données récupérées dans la base
    * J'ai créé la page index.php du site pour afficher les projets. J'ai utilisé la requête SQL *SELECT*. J'ai ensuite utilisé une boucle PHP *foreach* pour parcourir le tableau renvoyé par ma requête. J'ai utilisé une *card* de Bootstrap pour afficher mes projets.

        ![Capture d'écran de la page du site](https://i.ibb.co/R4c5z4x/indexfront.jpg)

    J'ai créé un formulaire de contact qui renvoie les informations à contact.php par la méthode *POST*. La fonction *array_key_exists()* vérifie si la clé *errors* existe et affiche le message d'erreur dans contenu dans $_SESSION['errors'].

    * La page contact.php traite les informations renvoyée par la méthode *POST*. J'ai définie une variable *$errors qui est un tableau vide que j'ai remplie de message d'erreur lorsque les champs ne sont pas renseignés. Lorsque l'erreur existe, je stock les données dans $_SESSION['inputs] et $_SESSION['errors] et les transvases vers footer pour arrêter le processus avec *unset()*.  Dans le cas contraite, si il n'y a pas d'erreur, le mail est envoyé avec succès.

    ![Capture d'écran de la page du site](https://i.ibb.co/1QZ1xmk/contact.jpg)





## Présentation du jeu d’essai 

Je vais soumettre à l'application quelques scénarios opérationnels afin de démontrer que les fonctionnalités attendues sont disponibles sur l'application: 

1. je me connecte connexion au back-office : par sécurité pour se connecter il faut obtenir le lien du back-office. Il n'existe pas de lien visible sur le front pour y accéder. J'ai donc renseigné mon nom d'utilisateur et mon mot de passe.

    ![Capture d'écran de la page connexion ](https://i.ibb.co/yq9SDWb/jeuessaiconnexion.jpg)


    Je tombe bien sur la page de liste de mes projets dans le back-office 

    ![Capture d'écran de la page home](https://i.ibb.co/jVNTSmZ/pagehome.jpg)
     

2. j'ajoute un projet : dans la page liste des projets, je clique sur le bouton "ajouter un projet". Je suis dirigé vers la page d'ajout des projets. Je reseigne les valeurs attendus dans les champs. Et j'envoi les données.

    ![Capture d'écran de la page home](https://i.ibb.co/djBCtZY/ajoutjeudessai.jpg)

3. Je vérifie que le projet est bien enregistrée en base de données : je me connecte à phpmyadmin et consulte dans ma table `projects` la liste des projets enregistrées en base. 

    ![Capture d'écran de la page home](https://i.ibb.co/KjwyZJq/ajoutenbasejeudessai.jpg)

4. je vérifie que le projet s'affiche parmis la liste des projets dans le back-office : j'accède à la page home.php consulte la liste.

    ![Capture d'écran de la page home](https://i.ibb.co/DLfqLS8/ajoutlisteprojetjeudessai.jpg)

5. je vérifie que le projet s'affiche dans la liste des projets dans le front-office : je visite la page index.php du site et consulte la liste des projets

    ![Capture d'écran de la page home](https://i.ibb.co/DRGmLqf/projetenfront.jpg)

6. je modifie un projet : je peux faire cette opération en allant sur la page home.php et cliqué sur l'icone "modifier" dans la colonne des "actions" soit en cliquant sur l'icone "consulter" puis dans cette page " je clique sur l'icone "modifier". Une fois arrivé sur le formulaire de modification, je renseigne les champs que je veux modifier. Dans le cas présent, je modifie les technologies, j'ajoute PHP à ma liste et j'envoi. 

    ![Capture d'écran de la page home](https://i.ibb.co/RbjR0Wb/modificationjeudessai.jpg)
    ![Capture d'écran de la page home](https://i.ibb.co/CwVyNjy/modifjeudessai.jpg)
    ![Capture d'écran de la page home](https://i.ibb.co/c3jFJwD/modificatinfront.jpg)

7. Je supprime un projet : la suppression se fait par clique sur l'icone "supprimer" de la page. Je vais supprimé le projet intitulé test. Je montre à la première et deuxième image que le projet existe dans la page home.php et en base de données. Puis les images trois et quatre montrent qu'après l'avoir supprimé, le projet n'existe plus dans les deux tables. 

    ![Capture d'écran de la page home](https://i.ibb.co/n1rrTwf/supprjeudessai.jpg)
    ![Capture d'écran de la page home](https://i.ibb.co/9YtPcgy/supprbase.jpg)
    ![Capture d'écran de la page home](https://i.ibb.co/cxX7Qm6/supprjeudessai1.jpg)
    ![Capture d'écran de la page home](https://i.ibb.co/60ShSs2/supprbase2.jpg)































































