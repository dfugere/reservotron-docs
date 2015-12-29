# Ajoutez Réservotron sur votre site et Intégration

Vous pouvez ajouter Réservotron directement sur votre site web pour faciliter la redirection de vos clients vers la réservation en ligne. Pour cela il suffit de suivre les étapes suivantes:

1. Ouvrez la page de votre compte Réservotron
1. Cliquez sur le bouton “Accueil” dans le coin supérieur gauche
1. Copier l’adresse URL qui s’affiche 
1. Insérer un lien sur votre site web vers le lien de la page d’inventaire (URL) de votre compte Réservotron que vous venez de copier 




![](https://monosnap.com/file/AcS8TtdsswphjOL9a03b57RtS8ffjV.png)

##Intégration

Si vous ne désirez pas rediriger vos clients vers la page de votre compte Réservotron, vous pouvez insérer un widget dans le code de votre site web. Celui-ci vous permettra d'ajouter le panier d'achat directement à votre site et d'effectuer les transactions sans avoir à le quitter.

1. Accédez au code de votre site web
2. Ajoutez le code suivant à l'intérieur de votre balise : 
<iframe id="reservotron-shopping-cart" src="http://staging.reservotron.com/cime-aventures/widgets/cart" frameborder="0" width="222" height="50"></iframe>                  
       <script async type="text/javascript" src="[http://localhost:3000/assets/widget.js](http://localhost:3000/assets/widget.js)"></script>
3. Attention: il faut remplacer "cime-aventures" par le nom de votre compte Réservotron tel qu'il figure dans le URL de ce dernier.
4. Enregistrez les modifications apportées au code