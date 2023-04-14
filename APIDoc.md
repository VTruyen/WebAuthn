# API Doc

# Primitives
Les primitives pour les mécaniques d'enregistrement et d'authentification sont respectivement create() et get()
> Remarque: Ces primitives sont utilisés dans le cadre de programme JS

# Etapes Appels Enregistrement 

**Etape 0**: Requete initialle d'enregistrement au server  
**Etape 1**: Reponse du server avec un objet JS *PublicKeyCredentialCreationOptions* qui contient le **challenge** destiné à l'**authentificateur**, les informations **utilisateur** et les informations du **tiers de confiance**  
**Etape 2**: Le navigateur fait un appel l'authentificateur  
**Etape 3 et 4**: L'authentificateur créé la paire de clé après vérification, le credential id et une attestation dans un objet JS *attesttationObject*
**Etape 5**: Le navigateur créé les data finales et les envoi au server sous la forme d'un *AuthenticatorAttestationResponse*

> Les etapes sont presques identiques pour la partie `Authentification`, les gros changement sont au niveau du contenu des objets JS échangés.

# Accès aux Objets JS
Voila un snippets de code JS qui montre comment l'élément `PublicKeyCredential`:
```javascript
if (window.PublicKeyCredential) {
        PublicKeyCredential.isUserVerifyingPlatformAuthenticatorAvailable().then(
```

# Liens importants
[Test compatibilité via script](https://webauthn-8276-dev.twil.io/supported.html) : voir dans la console le script complet de la page qui récupère le `PublicKeyCredential`