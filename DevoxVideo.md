# Devox Video

# Resume
## Mot de Passe
Les mots sont le système le plus répandue d'authentification, mais il comporte de nombreux défauts :
- ils sont réutilisés
- les gens utilisent souvent les mêmes (**ex:** *12345,11111,...*) 
- ils sont échangés (*connaisances, collègues,...*)
- on se sait pas comment ils sont gérer par les sites qui les stockent
- ils sont difficilement gérable quand changés souvent

Ils sont un moyen d'authenfication qui est basé sur la **connaissance** (voir section [Moyen Authentifiaction](#moyen-dauthenfication))  
On cherche donc à *Sécuriser* son mot de passe avec diverses moyens. 

## *Sécuriser* un mot de passe
Pour *sécuriser* un mot de passe il y a plusieurs moyens :
- la double Authentification (OTP -> One Time Password)
- le **TOPT** toujours le principe de du OTP
- le **TLS** (*necessite un midlleware qui complique l'utilisation*)

C'est de cette necessité de sécurité qu'est né **WebAuthn**

## WebAuthn
WebAuthn est donc un standard (*donc valable sur beaucoup de navigateur*) basé sur 2 primitives JS :
```javascript
    credentials.create()
    credentials.get()
```
Qui elles mêmes se basent sur le principe de cryptographie asymétrique (comme le chiffrement et surtout la **SIGNATURE**)  
En effet dans le mécanisme (Authentification et Enregistrement), le serveur envoi un challenge qui est une *épreuve* unique et aléatorie, à résoudre pour l'authentificateur et sera ensuite renvoyé et **SIGNÉ** par celui-ci. Le serveur fait ensuite ses vérifications et ermine la procédure. Voir détails de la spéc [ici](/APIDoc.md)

## Pertinence des clés

Les clés sont générées à la volé de manière beaucoup plus aléatoire. Seule la clée publique est partagée qui garantit l'intégrité de la clé privée. 

## Moyen d'authenfication
Il y a 3 grandes famille de moyen d'authenfication que sont :
- ceux basé sur la connaissance (*Mot de passe*)
- ceux basé sur ce que l'on possède (*Clé USB, SMS par téléphone*)
- ceux basé sur ce que l'on est (*Données Biométrique*)


# Lien Importants
[Lien Video](https://www.youtube.com/watch?v=AaiyuWSly60) : Conférence de Arnaud Locquet sur les principes du WebAuthn