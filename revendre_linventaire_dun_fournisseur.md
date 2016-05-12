# Revendre l'inventaire d'un fournisseur

Il est possible de partager l'inventaire d'un fournisseur à un autre revendeur. 

####Le revendeur aura la possibilité de: 
1. Publier l'inventaire partagé en ligne et prendre des réservations de ses clients via son compte Réservotron
2. Publier votre inventaire partagé et prendre des réservations de ses clients sur son site Web ([via le widget](ajouter_reservotron_sur_votre_site.md))
3. Réserver lui-même sur son compte Réservotron. 
4. Automatiser l'intégration avec l'API via son compte Reservotron.

##Création d'un catalogue et assignation du catalogue à des revendeurs
Pour créer un catalogue, suivez les étapes suivantes:
1. Allez dans Menu → Inventaire → Catalogues
2. Cliquez sur **AJOUTER CATALOGUE**
3. Ajoutez un nom pour votre catalogue
4. Saisissez le pourcentage de la commission du revendeur. *Si vous désirez spécifier une commission différente par item, laissez cette case vide.*
5. Cochez dans les listes les items que vous désirez partager avec le revendeur. Si vous voulez spécifier une commission par item, ajoutez le pourcentage à côté du nom de l'item en question. 
6. Sélectionnez un **revendeur** dans la liste déroulante. - *Vous pouvez rajouter autant de revendeurs que désiré*. Cette option permettra au revendeur d'avoir accès à l'inventaire que vous désirez partager avec lui.
7. Validez le tout en cliquant sur **CREÉR CATALOGUE**.


![](Screen Shot 2015-11-04 at 11.27.10 AM.png)


****

##Afficher l'inventaire partagé par des fournisseurs sur un compte de revendeur

Une fois l'inventaire du founisseur partagé, vous pouvez l'afficher en ligne en tant que revendeur via votre compte Réservotron. 

Pour ajouter l'inventaire partagé, suivez les étapes suviantes:

1. Allez dans Menu → Inventaire → Inventaire partagé
2. Vous verrez une liste des items que le fournisseur a partagé avec vous.
3. Dans chaque case blanche, sélectionnez la catégorie à laquelle vous voulez rajouter l'item
4. Répétez cette étape pour l'ensemble des inventaires partagés par des fournisseurs
5. Sauvegardez les changements


![](Screen Shot 2015-11-04 at 2.04.39 PM.png)


****

##Intégration automatisée avec Reservotron

Vous pouvez utiliser l'API de Reservotron pour automatiser les réservations en temps réel directement dans l'inventaire de vos founisseurs. 

La documentation technique de l'API se trouve ici : [https://reservotron.com/swagger-ui/#/default](https://reservotron.com/swagger-ui/#/default)

Si vous êtes un fournisseur et que vous désirez qu'un de vos revendeurs intègre son système de réservation avec votre compte Reservotron, vous devrez : 

1. Créez un compte pour le revendeur
2. Partagez l'inventaire désiré avec le compte du revendeur
3. Partager cette documentation avec le revendeur pour qu'il puisse configurer la communication avec Reservotron.  


####L'API permettra au revendeur de :
1. Faire des requêtes automatisée pour connaître vos disponibilités en temps réel
2. Créer automatiquement des réservations pour les activités disponibles


####Procédure de réservation automatisée par un revendeur :

2. Téléchargez la liste de produits via la route GET /products. La réponse inclut les attributs "product_id" et "participant_types" qui doivent être utilisés pour la réservation.
2. Téléchargez les disponibilités d'un produit via la route GET /occurrences/{productId}.  L'information importante de cette requête est "openings", "start_at", "end_at"
3. Créez une réservation via POST /bookings . Les attributs nécessaires pour la réservation sont disponibles ici : https://reservotron.com/swagger-ui/#!/default/post_bookings

