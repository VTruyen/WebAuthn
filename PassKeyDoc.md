# PassKey Doc

# Principe de Fonctionnement 
Contrairement aux autres système FIDO qui necessite le device particulier pour pouvoir s'authentifier de manière sure. Le principe de **PASSKEY** est de conserver une clé unique mais sur un clouds.

# Avantages / Désavantages
## Avantages
- Utilise les mêmes système de **WebAuthn** que les **authentificators** *classiques*
- Permet une meilleur *User Experience* grâce au principe de clé stocké en cloud.
- Moins *onéreux* que les autres système de WebAuthn/CTAP 
- Une Passkey peut être utiliser pour en générer une **autre** sur une **platforme totalement différente**
- Sert à promouvoir le *modèle* FIDO
- Utilise comme terminaux de base les **téléphones**

## Désavantages
- Moins sécurisée que les autres systèmes FIDO avec lien entre-device car la clé est présente dans un cloud donc **en ligne** ( *voir* [lien](/images/security_spectrum.png))
- Enferme un peu l'utilisateur dans le système cloud dans lequel se trouve la Passkey

# Objectif
L'objectif innitial des passkeys et comme d'autres système FIDO2 de **remplacer les mots de passes** à termes. Mais d'une manière un peu plus simple à appréhender pour les utilisateurs. Notamment en mettant en place un système ***cross platform***

# Liens Importants
[Pass Key In Action](https://www.youtube.com/watch?v=SWocv4BhCNg) : vidéo de la FIDO Alliance sur le fonctionnement des *passkey* (demo)  
[FIDO Passkey Primer IBM](https://www.youtube.com/watch?v=wN5lpttf_Hc) : vidéo qui revient en détails sur la démonstration de la vidéo précédente