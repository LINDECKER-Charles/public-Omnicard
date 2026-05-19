# Politique de cookies

**Dernière mise à jour : 17 mai 2026**

La présente politique décrit les cookies et traceurs utilisés sur `omnicard.fr` et ses sous-domaines, conformément à la directive 2002/58/CE (« ePrivacy »), à l'article 82 de la loi Informatique et Libertés et aux lignes directrices et recommandations de la CNIL relatives aux cookies et autres traceurs.

## 1. Qu'est-ce qu'un cookie ?

Un cookie est un petit fichier texte déposé sur le terminal de l'utilisateur (ordinateur, smartphone, tablette) par le navigateur, à l'occasion de la consultation d'un service en ligne. Il permet, pendant sa durée de validité, de reconnaître le terminal lors d'une nouvelle visite ou de stocker des informations relatives à la navigation.

La présente politique couvre, par extension, les autres mécanismes de stockage local utilisés par le service (`localStorage`, `sessionStorage`, `IndexedDB`), assimilés à des traceurs par la CNIL.

## 2. Principe : pas de traceur publicitaire ni d'analytics tiers

Omnicard n'utilise **aucun cookie publicitaire, aucun outil d'analyse comportementale tiers (Google Analytics, Meta Pixel, etc.) et ne revend aucune donnée à des fins marketing**. Seuls des traceurs strictement nécessaires au fonctionnement du service sont déposés, sans consentement préalable requis (article 82 al. 2 de la loi Informatique et Libertés).

Si cette politique évolue (ajout d'un outil de mesure d'audience, par exemple), un bandeau de consentement conforme aux exigences de la CNIL sera mis en place et l'utilisateur informé.

## 3. Inventaire des cookies et traceurs utilisés

### 3.1 Strictement nécessaires (pas de consentement requis)

| Nom / clé | Type | Finalité | Durée |
|---|---|---|---|
| Token de session JWT (cookie httpOnly ou storage selon implémentation) | Authentification | Maintenir la session utilisateur connecté | Durée du JWT (typiquement quelques heures à quelques jours) |
| Refresh token | Authentification | Renouveler le JWT sans re-login | Quelques jours à quelques semaines |
| `omnicard.theme` (localStorage) | Préférence UI | Mémoriser le thème clair / sombre choisi | Persistant tant que l'utilisateur ne l'efface pas |
| Préférences d'affichage (langue, layout deck builder…) | Préférence UI | Restaurer la mise en page entre sessions | Persistant |
| Token CSRF | Sécurité | Protection contre les attaques cross-site request forgery | Session |
| Cookie de répartition de charge (si applicable côté hébergeur) | Technique | Routage stable vers le bon nœud applicatif | Session |

Ces traceurs sont **indispensables** au fonctionnement du service. Les refuser empêche notamment de rester connecté, de conserver ses préférences, ou de protéger le compte contre certaines attaques.

### 3.2 Mesure d'audience interne (exempt de consentement sous conditions)

Si une mesure d'audience strictement limitée à l'amélioration du service est mise en place (`omnicard.fr` uniquement, sans recoupement, sans transmission à des tiers), elle relève de l'exemption prévue par les lignes directrices CNIL. Aucun outil de ce type n'est actuellement déployé.

### 3.3 Traceurs nécessitant consentement

À la date de mise à jour de la présente politique : **aucun**.

Si un tel traceur venait à être introduit (mesure d'audience non exemptée, intégration tiers, etc.), un bandeau de consentement permettrait à l'utilisateur :

- D'accepter,
- De refuser (refus aussi accessible visuellement que l'acceptation),
- De personnaliser finalité par finalité.

Le consentement, ses preuves et l'éventuel retrait seraient documentés conformément aux exigences CNIL.

## 4. Gestion par l'utilisateur

### 4.1 Via le navigateur

L'utilisateur peut configurer son navigateur pour bloquer, supprimer ou être averti des cookies déposés :

- **Chrome / Edge** : `Paramètres → Confidentialité et sécurité → Cookies et autres données des sites`
- **Firefox** : `Paramètres → Vie privée et sécurité → Cookies et données de sites`
- **Safari** : `Préférences → Confidentialité`
- **Mobile** : équivalents dans les paramètres du navigateur ou de l'application.

Le blocage des cookies strictement nécessaires rend le service partiellement ou totalement inopérant (impossible de rester connecté, perte des préférences).

### 4.2 Suppression du stockage local

Les données en `localStorage` peuvent être effacées via les outils de développement du navigateur ou en supprimant les données du site pour `omnicard.fr`.

### 4.3 Déconnexion et suppression de compte

La déconnexion invalide le token de session courant. La suppression du compte (depuis le profil) efface également les préférences associées côté serveur.

## 5. Cookies tiers

À la date de mise à jour des présentes, le service ne dépose **aucun cookie tiers**. Si des intégrations tierces venaient à être ajoutées (lecteur vidéo embarqué, fournisseur SSO, etc.), la liste serait mise à jour ci-dessus avec les liens vers les politiques de confidentialité des tiers concernés.

## 6. Évolution

Toute modification de la présente politique sera mise en ligne, datée, et notifiée le cas échéant. Pour toute question : `contact.omnicard@gmail.com`.

## 7. Plus d'informations

- CNIL — cookies et autres traceurs : `https://www.cnil.fr/fr/cookies-et-autres-traceurs`
- Politique de confidentialité Omnicard : [`politique-confidentialite.md`](politique-confidentialite.md)
