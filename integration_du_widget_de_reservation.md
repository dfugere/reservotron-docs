# Intégration du widget de réservation


Si vous ne désirez pas rediriger vos clients vers la page de votre compte Réservotron, vous pouvez insérer un widget dans le code de votre site web. Celui-ci vous permettra d'ajouter le panier d'achat directement à votre site et d'effectuer les transactions sans avoir à le quitter.

Nous avons créé une intégration simple sur une page HTML indépendante. Vous pourrez vous y référer à [titre d'exemple](https://github.com/codegenome/reservotron_widget/blob/86cc29ce4bb29071162bebc3901c47360196adad/demo.html). Voici le lien vers le code source : https://github.com/codegenome/reservotron_widget.

Voici un tutoriel vidéo d'intégration de Réservotron sur votre site wordpress : https://youtu.be/2Sq68Xy6xFc

Voici une description des étapes à suivre :

1. Accédez au code de votre site web
2. Ajoutez le code suivant dans l'entête à l'intérieur de votre balise body: 

    ```< iframe id="reservotron-shopping-cart" src="https://reservotron.com/votre-identifiant/widgets/cart" frameborder="0" width="222" height="50"></iframe> ```                 
    ```<script async type="text/javascript" src="http://reservotron.com/assets/widget.js"></script>
```

3. Ajoutez ensuite le code suivant à la fin de votre page d'activités : 

    ```< iframe id="reservotron-store-content" src="https://reservotron.com/votre-identifiant?c=1107&widget=1" frameborder="0" width="900" height="700"></iframe>```
    
4. Attention: dans les deux cas, il faut remplacer "votre-identifiant" par le nom de votre compte Réservotron tel qu'il figure dans le URL de ce dernier.
4. Enregistrez les modifications apportées au code
5. Rafraichissez votre site web. Vous verrez le panier d'achat apparaitre directement dans le site. Vos clients pourront effectuer les transactions sans avoir à le quitter.




