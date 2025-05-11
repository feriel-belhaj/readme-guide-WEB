# readme-guide-WEB
Guide détaillé pour notre projet (application web)appelé Artizina sous  le thème de l'art 

# ARTIZINA

Une plateforme web innovante dédiée à la promotion de l’ARTISANAT TUNISIEN, développée avec SYMFONY 6.4, PHP,et intégrant des APIs avancées (STRIPE, HUGGING FACE, DANDELION, CHATBASE, FACE API, GOOGLE GEMINI, EDENAI) pour la gestion des utulisateurs, paiements, portfolios, candidatures, et un chatbot personnalisé.

# DESCRIPTION
ARTIZINA est une plateforme web réalisée dans le cadre du PROJET INTÉGRÉ WEB JAVA de la 3ÈME ANNÉE, CLASSE A44 à ESPRIT SCHOOL OF ENGINEERING, sous la direction du PROFESSEUR SAFOUENE ZOUARI. Elle vise à promouvoir l’ARTISANAT TUNISIEN en offrant une gestion intuitive des utilisateurs, produits, évènements, formations, partenariats, et créations. Construite avec SYMFONY, PHP, MYSQL, JAVASCRIPT, CSS, TWIG et BOOTSTRAP, elle intègre des APIs avancées :

STRIPE pour les paiements (achats, dons).
HUGGING FACE pour évaluer les portfolios artistiques.
DANDELION pour analyser les lettres de motivation.
CHATBASE pour un chatbot frontend personnalisé.
FACE API pour l’authentification via FACE ID.
GOOGLE GEMINI et EDENAI pour l’analyse de contenu/images (rôles supposés).
Systéme de fideletié pour reduire les prix et promouvoir les ventes 
Prototype d’un modèle 3D du produit developpe dans le cadre du formation
Affichage de la localisation du lieu de formation sur une carte interactive.
Système de prédiction permettant d’évaluer si la formation correspond ou non aux besoins du client.
Intelligence Artificielle pour des analyses avancées.
Des fonctionnalités de sécurité incluent le HACHAGE DES MOTS DE PASSE (bcrypt), des E-MAILS (bienvenue, réinitialisation), et un ESPACE PERSONNEL avec gestion des sessions.
Affichage de la localisation du lieu de l’évènement sur une carte interactive.
Affichage de la météo d’aujourd’hui et prévision de la météo du 1er jour de l’évènement.
Dashboard interactive et dynamique même style qu’une Dashboard Power Bi.

# Principales fonctionnalités

GESTION DES UTILISATEURS : Inscription avec e-mail de bienvenue, connexion via FACE ID ou mot de passe, déconnexion, espace personnel avec détails , gestion des sessions.
GESTION DES PRODUITS ARTISANAUX : store permettant aux clients de parcourir et sélectionner les produit artisanaux disponibles,panier pour consulter et gérer les produits ajoutés avant la validation de commande , paiement sécurisé via l’API Stripe et envoi automatique d’un e-mail de confirmation après chaque commande efféctués.


GESTION DES ÉVÈNEMENTS ET DONS : Organisation d’expositions et dons via STRIPE.
GESTION DES FORMATIONS ET CERTIFICATS : Cours en présentielle avec certificats (supposés en PDF).
GESTION DES PARTENARIATS ET CANDIDATURES : CRUD pour les partenariats , liste et candidature pour clients (portfolios évalués par HUGGING FACE, motivations analysées par DANDELION).
GESTION DES CRÉATIONS ET COMMENTAIRES : Publication d’œuvres avec commentaires.

Gestion des Creation/Commentaire

Génération d’œuvres via formulaire ou import direct, prévisualisation en temps réel, prise en charge des fichiers multimédias (image, audio, vidéo), assignation à une catégorie existante, détection automatique du type de contenu, gestion des métadonnées (titre, description, tags), sauvegarde en brouillon ou publication immédiate, et attribution automatique à l’utilisateur connecté.



# Rôles des utilisateurs

ADMIN : Gère tous les CRUD (créer, lire, mettre à jour, supprimer) pour toutes les entités (utilisateurs, produits, évènements, formations, partenariats, créations).
ARTISAN : 
-Gère les CRUD DES PARTENARIATS (ajouter, modifier, supprimer, afficher), les candidatures reçues, et publie des PRODUITS ARTISANAUX et CRÉATIONS.
-gestion de stock compléte avec alerte en cas de repture.
-exportation pdf des commandes
-suivre les ventes et le chiffres d’affaires grâce à des statistiques interactives et détaillées
-Ajout d’évènements.

CLIENT :
-Consulte la liste des partenariats, postule à un partenariat, et gère ses candidatures (modifier, supprimer) dans l’ESPACE PERSONNEL.
-parcourir et sélectionner les produit artisanaux disponibles.
-consulter et gérer les commandes  ajoutés dans le panier  avant la validation de commande 
-Accès à la liste des formations proposées, avec des options de tri et de recherche, et réservation directe via la plateforme.
-Accès à la liste des évènements proposées, avec des options de tri et de recherche, et Faire des dons directe via la plateforme.



# TABLE DES MATIÈRES

INSTALLATION
UTILISATION
CONTRIBUTIONS
LICENCE


# INSTALLATION

Suivez ces étapes pour configurer ARTIZINA localement avec XAMPP et VS CODE:

1. Clonez le dépôt depuis GITHUB :git clone https://github.com/feriel-belhaj/PIDEV.git
cd PIDEV


2. Placez le projet dans le dossier htdocs de XAMPP (par exemple, C:\xampp\htdocs\PIDEV).
Installez les dépendances avec COMPOSER :composer install


3. Installez les assets frontend avec NPM :npm install


4. Copiez .env.example en .env et configurez pour MYSQL et les APIs :DATABASE_URL="mysql://root@127.0.0.1:3306/artizina3"
STRIPE_SECRET_KEY=""
STRIPE_PUBLIC_KEY=""
HUGGING_FACE_API_KEY=""
DANDELION_API_KEY=""
FACE_API_KEY=""
FACE_API_SECRET=""
GEMINI_API_KEY=""
EDENAI_API_KEY=""
MAILER_DSN=""


* Note :  Ne committez pas .env dans le dépôt public ; utilisez .env.example pour les clés fictives.
Exécutez les migrations pour créer la base de données :php bin/console doctrine:migrations:migrate


5. Démarrez  MYSQL depuis l’interface de XAMPP.
Accédez au projet via :http://localhost/PIDEV


6. Utilisez VS CODE pour modifier le code ou le README.


# Prérequis

XAMPP (Apache et MySQL activés)
PHP 8.1 ou supérieur (inclus dans XAMPP)
MYSQL 5.7 ou supérieur (inclus dans XAMPP)
COMPOSER
NODE.JS (pour les assets frontend)
GIT
VS CODE
Clés API pour STRIPE, HUGGING FACE, DANDELION, CHATBASE, FACE API, GOOGLE GEMINI, EDENAI
Service SMTP (GMAIL configuré)


Installation de PHP (si hors XAMPP)
Si vous n’utilisez pas XAMPP :

Windows : Téléchargez PHP depuis php.net.



Vérifiez l’installation :php -v




# UTILISATION


1. Accédez à l’application via http://localhost/PIDEV.
2. Créez un compte (un E-MAIL DE BIENVENUE sera envoyé) ou connectez-vous avec FACE ID (via webcam) ou mot de passe.
Explorez les modules dans l’ESPACE PERSONNEL, selon votre compte :
* ADMIN :
Gère tous les CRUD pour les utilisateurs, produits, évènements, formations, partenariats, et créations.


* ARTISAN :
Gère les CRUD DES PARTENARIATS (ajouter, modifier, supprimer, afficher).
Gère les candidatures reçues.
Publie des PRODUITS ARTISANAUX et CRÉATIONS.
Publication des formations et attribution des certificats
Publication d’evenements.

* CLIENT :
Consulte la LISTE DES PARTENARIATS.
Postule à un partenariat (candidature visible dans l’ESPACE PERSONNEL).
Modifie ou supprime ses candidatures (portfolio évalué via HUGGING FACE API, motivation analysée via DANDELION API).
Accès à la liste des formations proposées, avec des options de tri et de recherche, et réservation directe via la plateforme.
Accès à la liste des évènements proposées, avec des options de tri et de recherche, et Faire des dons directe via la plateforme.




4. AUTRES MODULES :
PRODUITS ARTISANAUX : Achetez des produits avec STRIPE.
ÉVÈNEMENTS ET DONS : Participez à un évènement ou faites un don via STRIPE.
FORMATIONS ET CERTIFICATS : Suivez un cours et recevez un certificat (PDF supposé).
CRÉATIONS ET COMMENTAIRES : Interagissez avec les œuvres via le CHATBOT CHATBASE (frontend).
ESPACE CONTACT: Envoyez des messages à l’administration via un formulaire. Admin gère les messages (CRUD), liste paginée, exportable, avec statistiques (messages reçus, réponses).



5. En cas de MOT DE PASSE OUBLIÉ, recevez un code de réinitialisation par e-mail.
6. Utilisez VS CODE pour personnaliser le code.


# CONTRIBUTIONS

Nous remercions tous les contributeurs pour leur travail sur ARTIZINA, réalisé dans le cadre de la 3ÈME ANNÉE, CLASSE A44 à ESPRIT SCHOOL OF ENGINEERING, sous la direction du PROFESSEUR SAFOUENE ZOUARI.

# Contributeurs

FATMA ZAHRA CHAKROUN : Gestion des utilisateurs (inscription, connexion, Face ID, e-mails).
FERIEL BEL HADJ JAMMAR : Gestion des partenariats et candidatures (CRUD, analyse via Hugging Face/Dandelion).
RAWEN MEZZI : Gestion des formations et certificats (cours, génération de certificats).
TAOUFIK KRID : Gestion des produits artisanaux (catalogue, paiements Stripe).
ANAS ALLAM : Gestion des évènements et dons (organisation, paiements Stripe).
YOUSSEF FADDEOUI : Gestion des créations et commentaires, intégration du chatbot Chatbase.


# Comment contribuer ?

1. Fork le projet : Cliquez sur "Fork" sur https://github.com/feriel-belhaj/PIDEV.
2. Clonez votre fork :git clone https://github.com/feriel-belhaj/PIDEV.git
cd PIDEV


3. Créez une nouvelle branche :git checkout -b votre-fonctionnalite


4. Faites vos modifications dans VS CODE et validez-les :git add .
git commit -m "Ajout de votre-fonctionnalite"


5. Poussez vos modifications :git push origin votre-fonctionnalite


6. Soumettez une PULL REQUEST sur GITHUB en décrivant vos changements.


# LICENCE
Pas de licence pour notre projet .

# Mots-clés :
SYMFONY, PHP, ARTISANAT TUNISIEN, STRIPE PAYMENT API, HUGGING FACE API, DANDELION API, CHATBASE, FACE ID, GOOGLE GEMINI API, EDENAI API, HACHAGE MOT DE PASSE, E-MAIL NOTIFICATION, DÉVELOPPEMENT WEB, ESPRIT SCHOOL OF ENGINEERING, JAVASCRIPT, CSS, TWIG, BOOTSTRAP, XAMPP, VS CODE, GESTION DES PARTENARIATS, ESPACE PERSONNEL, CHATBOT FRONTEND, PAGINATION, EXPORT PDF/EXCEL, STATISTIQUES, ESPACE CONTACT, systéme de fidélité,facture,chiffre d’affaire,TVA,QR code , modèle 3D ,openstreetmap


