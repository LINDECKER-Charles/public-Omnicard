# Mode Classé — Échelle Cosmique

Le mode Classé d'Omnicard est une **file de matchmaking** où chaque victoire ou défaite ajuste tes **Étincelles**. Les Étincelles déterminent ton palier sur l'**Échelle Cosmique**, un classement à 8 paliers thématisés.

---

## Les 8 paliers

| # | Palier | Étincelles | Tag équivalent |
|---:|---|---|---|
| 1 | Poussière Stellaire | 0 – 199 | Bronze I |
| 2 | Astéroïde | 200 – 499 | Bronze II |
| 3 | Comète | 500 – 999 | Argent |
| 4 | Planète | 1 000 – 1 599 | Or |
| 5 | Étoile | 1 600 – 2 299 | Platine |
| 6 | Nébuleuse | 2 300 – 2 999 | Diamant |
| 7 | Galaxie | 3 000 – 3 699 | Mythique |
| 8 | Singularité | 3 700+ | Apex |

**Pas de division interne** (pas de Bronze I/II/III, pas de promo series). Le palier est purement scalaire : atteindre le seuil bas suffit.

## Économie des Étincelles

| Évènement | Variation |
|---|---:|
| Victoire classée | **+24** |
| Défaite classée | **−18** |
| Décroissance d'inactivité (paliers Étoile+) | **−8** après 7 jours sans partie classée |

**Solde net à 50 % de winrate** : +3 Étincelles/partie. La progression est visible sur du volume mais reste honnête statistiquement.

**Décroissance d'inactivité** : seulement à partir d'**Étoile** (palier 5). Les paliers d'introduction ne sont pas pénalisés — défense de palier réservée à la zone élite.

## Plancher de palier

Recommandation de design : **plancher au seuil bas du palier courant** pour limiter les démotivations. Tu ne tombes pas du palier 3 au palier 2 par une mauvaise série, tant que tu restes au palier 3 par tes parties classées.

## Saisons

> Spec de design en cours. Une saison correspond à un cycle de classement avec reset partiel des Étincelles, récompenses cosmétiques de fin de saison, et titre commémoratif.

## Titres et cosmétiques

Chaque palier débloque un **titre cosmétique équipable** affiché à côté du pseudo. Les paliers 5-8 (Étoile, Nébuleuse, Galaxie, Singularité) bénéficient d'un cadre serti doré renforcé et d'un halo visuel sur le médaillon.

## Lore des paliers

| Palier | Sous-titre | Citation |
|---|---|---|
| Poussière Stellaire | Le commencement | *« Tu n'es qu'un fragment perdu dans le vide. »* |
| Astéroïde | Un caillou errant | *« Tu commences à exister. »* |
| Comète | On te remarque | *« Tu traces ta trajectoire dans la nuit. »* |
| Planète | Tu as une identité | *« Une masse, une gravité propre, une orbite. »* |
| Étoile | Tu brilles | *« Tu attires des choses dans ton orbite. »* |
| Nébuleuse | Tu crées | *« Une force créatrice — un berceau de mondes. »* |
| Galaxie | Tu contiens des milliards | *« Des milliards de possibilités tournent autour de toi. »* |
| Singularité | L'apex | *« Tu plies l'espace-temps autour de toi. »* |

## Statut d'implémentation

Le mode Classé devient **jouable à partir de la version 1.2.0 — Couronne** (cf. [`CHANGELOG.md`](../CHANGELOG.md)). Matchmaking ELO, Étincelles à chaque match, titres débloqués par palier — la base est là.

À venir (non implémenté à ce jour) : décroissance d'inactivité finalisée, structure de saison, récompenses de fin de saison.
