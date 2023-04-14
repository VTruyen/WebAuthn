# KeyCloackDoc

# Principe Général
## Conservation des clés

KeyCloack est un *module d'authentification* qui utilise le principe de paire de clés privée publique pour fonctionner. C'est  à dire que pour garantir le bon fonctionnement KeyCloak va conserver la clé publique de l'authentificateur en tant que *credential* et de son coté l'authentificateur va garder sa clée privée secrète.

## Cérémonie (*flow*)
KeyCloak dénombre 2 cérrémonies ou *flow* prinicpales que sont :
- l'enregistrement
- l'authentification
> Remarque: Pour plus de détails sur les procédures de chaque céremonie voir article

Les deux reposes sur les même principes car utilise la même [API](/APIDoc.md).


## Utilisation

KeyCloack fournit une solution paramètrable pour effectuer du WebAuthn. Donc pour réaliser notre système il faut réaliser les étapes suivantes :
- Créer un flow d'Authentification dans Keycloak
- Activer l'option d'autentification sans mot de passe (*passwordless*)
- On initalise le processus d'enregistrement et Keycloack envoi donc son challenge à l'authentificateur externe qui crée la paire de clé
- L'authentificateur lui renvoi ensuite une **Attestation** contient tout les inforamtions dont KeyCloack a besoin pour terminer le processus.
- KeyCloack fait ses vérifications et stocke la clé publique en tant que *crédential* sa base

# Lien importants
[KeyCloack Medium Article](https://medium.com/@rishabhsvats/webauthn-based-authentication-in-keycloak-a88c7c590e0f) : article qui détaille le fonctionnement de KeyCloack