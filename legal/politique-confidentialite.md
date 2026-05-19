# Politique de confidentialité

**Dernière mise à jour : 17 mai 2026**

La présente politique de confidentialité décrit la manière dont Omnicard (`omnicard.fr`) collecte, utilise et protège les données personnelles de ses utilisateurs, conformément au Règlement (UE) 2016/679 (RGPD) et à la loi Informatique et Libertés du 6 janvier 1978 modifiée.

## 1. Responsable de traitement

- **Responsable** : LINDECKER Charles, agissant à titre personnel non professionnel
- **Contact** : `contact.omnicard@gmail.com`
- **Site éditeur** : `https://charles-lindecker.com`
- **Délégué à la protection des données (DPO)** : non désigné — l'éditeur n'est pas soumis à cette obligation au sens de l'article 37 RGPD. Toute demande relative aux données personnelles peut être adressée directement au responsable à l'adresse ci-dessus.

## 2. Données collectées

### 2.1 Données fournies par l'utilisateur

| Donnée | Origine | Caractère |
|---|---|---|
| Adresse email | Inscription | Obligatoire |
| Mot de passe (haché BCrypt) | Inscription | Obligatoire |
| Pseudonyme | Inscription | Obligatoire |
| Avatar | Profil | Facultatif |
| Slug public (`/u/:slug`) | Dérivé du pseudo | Obligatoire |
| Biographie / liens sociaux | Profil | Facultatif |

### 2.2 Données générées par l'usage

| Donnée | Finalité | Caractère |
|---|---|---|
| Decks construits, brouillons | Fonctionnement du jeu | Nécessaire |
| Cartes possédées, ouvertures de packs | Collection joueur | Nécessaire |
| Historique de parties, statistiques | Classement, progression | Nécessaire |
| Liste d'amis | Fonctionnalité sociale | Facultatif |
| Logs techniques (Serilog) : IP, user-agent, timestamps | Sécurité, debug, anti-abus | Nécessaire |
| Date de dernière connexion | Sécurité, nettoyage de comptes inactifs | Nécessaire |

### 2.3 Données collectées automatiquement

- Adresse IP (logs serveur, rate-limiting, détection d'abus)
- User-agent du navigateur
- Cookies techniques (voir [politique-cookies.md](politique-cookies.md))

**Aucune donnée sensible** au sens de l'article 9 RGPD (santé, opinions politiques, orientation sexuelle, données biométriques…) n'est collectée.

## 3. Finalités et bases légales

| Finalité | Base légale | Conservation |
|---|---|---|
| Création et gestion du compte utilisateur | Exécution du contrat (art. 6.1.b) | Durée de vie du compte + 30 jours |
| Authentification (JWT, vérification email, reset password) | Exécution du contrat | Session active + tokens limités |
| Matchmaking et déroulé des parties | Exécution du contrat | Voir 3.2 |
| Affichage du profil public | Intérêt légitime (visibilité communauté) | Durée de vie du compte |
| Logs de sécurité et anti-fraude | Intérêt légitime (sécurité du service) | 12 mois maximum |
| Modération (signalements, bannissements) | Intérêt légitime + obligation légale | Voir 3.3 |
| Communication transactionnelle (email de vérif, reset, alerte sécurité) | Exécution du contrat | Durée de vie du compte |
| Statistiques anonymisées d'usage | Intérêt légitime | Indéfini (anonymisé) |

### 3.1 Comptes inactifs

Un compte sans connexion pendant **24 mois** est considéré inactif. L'utilisateur reçoit un email de relance et, en l'absence de réaction sous 30 jours, le compte est anonymisé (pseudonyme remplacé par `[joueur supprimé]`, email purgé, mot de passe invalidé). Les données de partie nécessaires aux historiques d'autres joueurs sont conservées sous forme désindexée.

### 3.2 Historique de parties

Conservé pendant **12 mois** glissants pour permettre le replay et la détection de comportements abusifs, puis purgé ou anonymisé.

### 3.3 Modération

Les éléments liés à un bannissement (motif, signalements, logs associés) sont conservés **3 ans** à compter du fait sanctionné, pour empêcher le contournement par re-création de compte et documenter l'application des [conditions d'utilisation](conditions-utilisation.md).

## 4. Destinataires

Les données ne sont **jamais vendues** ni cédées à des tiers à des fins commerciales.

Les sous-traitants ayant accès aux données strictement nécessaires à l'accomplissement de leur mission sont :

| Sous-traitant | Rôle | Localisation |
|---|---|---|
| Hostinger International Ltd. | Hébergement de l'infrastructure applicative, de la base de données et des assets statiques (`omnicard.fr`, `images.omnicard.fr`) | UE |

L'envoi des emails transactionnels (vérification de compte, réinitialisation de mot de passe, alertes de sécurité) est assuré par l'**infrastructure propre de l'éditeur**, sans recours à un service d'emailing tiers. Les adresses email ne sont transmises à aucun prestataire externe.

Aucun transfert hors UE n'est effectué. En cas d'évolution, l'utilisateur sera informé et les garanties appropriées (clauses contractuelles types, décision d'adéquation) seront mises en place.

## 5. Sécurité

L'éditeur met en œuvre les mesures techniques et organisationnelles appropriées pour protéger les données :

- Mots de passe hachés avec **BCrypt** (jamais stockés en clair).
- Authentification via **JWT** signés, durée de vie limitée.
- Connexions chiffrées **HTTPS / WSS** uniquement.
- Base de données et logs **non exposés publiquement**.
- Sauvegardes régulières.
- Journalisation des accès administrateur.
- Mise à jour régulière des dépendances et correctifs de sécurité.

En cas de violation de données susceptible d'engendrer un risque pour les droits et libertés des utilisateurs, l'éditeur notifiera la CNIL dans les **72 heures** et informera les personnes concernées si le risque est élevé, conformément aux articles 33 et 34 RGPD.

## 6. Droits des utilisateurs

Conformément au RGPD, chaque utilisateur dispose des droits suivants :

- **Accès** (art. 15) : obtenir copie de ses données.
- **Rectification** (art. 16) : modifier les données inexactes via le profil ou par demande.
- **Effacement** (art. 17) : suppression du compte depuis le profil ou par email. La fonctionnalité « suppression de compte RGPD » est intégrée à l'application.
- **Limitation du traitement** (art. 18).
- **Portabilité** (art. 20) : export des données du compte dans un format lisible par machine.
- **Opposition** (art. 21) au traitement fondé sur l'intérêt légitime.
- **Définition de directives post-mortem** sur le sort des données après décès (art. 85 loi Informatique et Libertés).

### Exercice des droits

Toute demande peut être adressée à `contact.omnicard@gmail.com`. Une réponse est apportée dans un délai d'**un mois**, prolongeable de deux mois en cas de demande complexe (avec information préalable).

### Réclamation auprès de la CNIL

À défaut de réponse satisfaisante, l'utilisateur peut introduire une réclamation auprès de la CNIL :

- En ligne : `www.cnil.fr/plaintes`
- Par courrier : CNIL — 3 Place de Fontenoy — TSA 80715 — 75334 PARIS CEDEX 07

## 7. Cookies

Le détail des cookies utilisés est précisé dans la [politique de cookies](politique-cookies.md).

## 8. Mineurs

Le service est ouvert aux personnes âgées de **13 ans révolus**. Il n'est en aucun cas destiné aux enfants de moins de 13 ans, et l'éditeur ne collecte pas sciemment de données les concernant.

Conformément à l'article 8 du RGPD et à l'article 45 de la loi Informatique et Libertés, le seuil de consentement numérique en France est fixé à **15 ans**. En conséquence :

- Les utilisateurs **âgés de 15 ans et plus** consentent eux-mêmes au traitement de leurs données personnelles.
- Les utilisateurs **âgés de 13 à 14 ans** doivent obtenir l'autorisation préalable d'un titulaire de l'autorité parentale pour s'inscrire et pour le traitement de leurs données. Cette autorisation est sollicitée lors de l'inscription, et l'éditeur se réserve le droit de demander toute pièce justificative.

Tout compte signalé comme appartenant à un enfant de moins de 13 ans, ou à un mineur de 13-14 ans sans autorisation parentale valide, sera suspendu puis supprimé à défaut de régularisation.

## 9. Modifications

La présente politique peut être modifiée pour refléter l'évolution du service, des obligations légales ou des sous-traitants. Toute modification substantielle est notifiée aux utilisateurs (email et/ou notification à la connexion) au moins **30 jours avant** son entrée en vigueur lorsque cela est requis.

## 10. Contact

Pour toute question : `contact.omnicard@gmail.com`.
