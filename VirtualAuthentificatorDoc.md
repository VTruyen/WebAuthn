# VirtualAuthentificatorDoc

# Fonctionnement Générale
Pour eviter de consommer des identifiants d'authentificateurs comme ceux qui pourrait se trouver sur une clé. 
Il est possible d'utiliser des **Authentificateurs virtuel**.

# Quelques détails

Si le navigateur est capatible alors la console de celui-ci embarque de manière native les outils permettant la génération d'Authentificateur virtuel.  
En outre une table des *credentials* est disponilble et vierge à la création de chaque Authentificateur. 
Pour créer l'Authentificateur il faut renseigner une certaine liste de paramètres : 
- protocol
- support
- différents flags (*residents key, user verification et large blob*)

Ensuite il faut lui assigner un *credential*.  
Il est possible de les exporter. -> *voir utilité*  
Enfin il faut activer l'authentificateur pour qu'il soit utilisable.

# Lien Importants
[Procédure officielle](https://developer.chrome.com/docs/devtools/webauthn/) : Montre la procdéure officielle avec le lien du site de démo  
[Test compatibilité navigateur](https://caniuse.com/?search=WebAuthn): site de Can I use, permettant de savoir si la version du navigateur est compatible avec WebAuthn