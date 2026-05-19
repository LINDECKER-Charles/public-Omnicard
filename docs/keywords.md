# Mots-clés et mécaniques

> Glossaire des mots-clés, attributs et mécaniques utilisés sur les cartes.
> Pour les règles de partie, voir [`rules.md`](./rules.md). Pour les types de cartes, voir [`card-types.md`](./card-types.md).

---

## Statuts de carte

- **Base** — la majorité des cartes. **3 exemplaires max** par deck.
- **Légendaire** — **1 exemplaire max** par deck.
- **Invocation** — générée uniquement par effets, ne se met pas directement dans le deck.

## Raretés

**Commun → Rare → Épique → Ultime**. Détermine les drops en pack et le coût de craft. N'a pas d'effet sur le moteur de jeu.

---

## Attributs persistants d'une unité

### Esquive(N)
Stack d'esquives. Chaque attaque reçue consomme **1 stack** et **annule entièrement** les dégâts. Première dans l'ordre de mitigation (avant Robustesse et avant Gear).

### Provocation
L'adversaire **doit cibler une unité Provocation** en premier s'il attaque. Ne bloque pas les sorts ciblés.

### Provocation Totale
Identique à Provocation côté ciblage. La distinction est narrative (« provocation impossible à contourner »).

### Anti-Magie
**Bloque tout Spell ciblé** sur cette unité. N'empêche pas les dégâts d'effets non-Spell (Gear, Ground, persistants).

### Robustesse(N)
Soustrait **N points fixes** au dégât reçu, clampé à 0. S'applique après Esquive.

### Espion(N)
Compteur d'espion. À 0, l'unité **change de propriétaire** (conserve son identité, ses stats, son gear).

### Compteur de dégâts
Compteur générique « tous les N dégâts infligés, … ». Utilisé par des cartes comme *Gilbert*, *La Veille Femme*, *Temple Inca*.

---

## Mots-clés de timing

### Entrée en Scène
Effet déclenché **à la pose** de la carte (Unit, Spell, ou Ground).

### Fin du Tour
Effet déclenché à **la fin du tour** du contrôleur de la carte. Concerne les unités sur le plateau et le Terrain actif.

### Dernier Souffle
Effet déclenché à **la mort** d'une unité.

### Délai(N)
Effet programmé pour s'exécuter **N tours plus tard**. Le compteur décrémente uniquement à la fin du tour du joueur qui a programmé l'effet. Si l'unité émettrice meurt, l'effet est annulé.

### Rechargement(N)
Effet **récurrent** qui se redéclenche tous les N tours (différent de Délai qui ne se déclenche qu'une fois).

### Quand / Chaque fois que
Effet persistant souscrit à un événement (carte jouée, unité morte, dégât subi, Extase gagnée…). Reste actif tant que la carte est dans sa zone d'activation.

### Assassinat
Effet déclenché quand l'unité **tue** une unité ennemie.

### Équipé
Effet conditionnel actif **uniquement quand l'unité porte un Gear**.

---

## Mots-clés de coût et de condition

### Extase
Ressource secondaire gagnée en infligeant des dégâts (+1 par point).

Notations sur les cartes :

| Forme | Sens |
|---|---|
| `Extase → X` | Coût variable que tu saisis à la pose |
| `Extase → N` | Coût fixe en Extase à payer en plus du mana |
| `Extase(N)` | Condition de seuil (lecture, sans dépense) |

### Initiale
Carte qui part en **main de départ** avant la pioche si sa condition d'éveil est satisfaite. Évaluée sur le deck construit, pas la pioche.

Exemples :
- *Atelier des Gemmes* — inconditionnel.
- *Atelier des Runes* — deck contient ≥ 6 Runes uniques.
- *Vasque : Lucidité* — deck contient ≥ 9 Offrandes uniques.

### Réutilisable(N)
La carte **retourne en main** après usage, **N fois**. À 0, va au cimetière normalement.

### Coût réduit
Réductions cumulatives sur le coût d'une carte selon différents critères :

| Réduction | Cible |
|---|---|
| Prochaine carte (one-shot) | Vision +1, Atelier du Chasseur Flame |
| Tous les Gear | Festival d'Urnes des Messagers |
| Tous les Pièges | Œdon Impalpable |
| Famille Grand | Mergot |
| Famille Ésotérisme | Gemme: Triangle 2 (Extase ≥ 10) |
| Famille Offrande | Vasque : Lucidité |
| Gear Outil ∧ Chasseur | Atelier des Armes |

---

## Effets sur les stats

### Affûtage(P, D)
Buff **tous les Gear portés** par tes unités de +P PV et +D Attaque.

### Régénération
Soin automatique en début ou fin de tour de l'unité porteuse.

### Frappe distante
L'attaque **ne déclenche pas de riposte**.

### Combat Proche
L'antonyme implicite. Certains effets visent spécifiquement les unités en Combat Proche.

### Bonus / Malus
+X/+Y ou -X/-Y sur les stats. La notation utilisateur sur les cartes est **Attaque/PV**.

### Enchantement
Bonus ou effet attaché à la vie d'une unité, supprimé automatiquement à sa mort.

### Buff global de famille
Effet qui propage un bonus à **toutes les copies d'une famille** chez le joueur — partout (main, deck, cimetière, plateau, pool d'invocations).

### Oblitérer
Supprime une carte qui **ne va pas au cimetière**.

### Défausse
Envoie une carte de la main au cimetière. Certaines cartes défaussent toute la main adverse, voire le deck entier.

---

## Attributs spéciaux

### Abyssal
La carte **ne va pas au cimetière** à sa consommation — elle est silencieusement détruite. L'effet est purement instantané, pas d'effet persistant cimetière possible.

### Incrustation
Marque un Gear comme **incrustable**. Il peut être attaché à un Gear principal (3 max), ou équipé seul si l'unité n'a pas de Gear.

---

## Familles thématiques

Les cartes peuvent appartenir à 1 ou 2 familles qui débloquent des synergies de deck.

### Côté Bloodborne

| Famille | Identité |
|---|---|
| **Chasseur** | Identité principale. ~40 cartes. Buffs Communion +4, Atelier des Armes, Eileen |
| **Grand** | Identité secondaire (« Great Ones »). Buffs Lune Sanglante, Cerveau de Mensis, Mergot |
| **Bête** | Cible de la Lame Sépulcrale |
| **Rune** | Compteur global, déclencheurs Card 172, 180, 181 |
| **Outil** | Gear utilitaire — combiné à Chasseur pour le discount Atelier des Armes |
| **Offrande** | Cartes Messagers principalement |
| **Ésotérisme** | Magie, cible des Gemmes Triangle |
| **Gemme** | Catégorie d'incrustation |
| **Sang**, **Rêve**, **Messager**, **Calice**, **Labyrinthe**, **Humain**, **Boss**, **Médecin**, **Lucidité**, **Yharnam** | Sous-tags thématiques |

### Côté JoJo

| Famille | Identité |
|---|---|
| **Joestar** | Identité Jojo Pt1. Synergies George, Danny, Jonathan, Speedwagon |
| **Vampire** | Antagonistes — Dio, Cimetière Abandonné |
| **Onde** | Hamon. Transformations Jonathan, Straizo |
| **Roublard** | Sous-tag |
| **Chevalier**, **Serpent**, **Justice**, **Chien** | Sous-tags narratifs |

### Côté WTF

| Famille | Identité |
|---|---|
| **Singularité** | Identité Floppa |
| **Mage**, **Guerrier**, **Assassin** | Sous-classes Floppa |
| **Chat** | Sur les traces de Floppa |
| **Démon**, **Malédiction** | Sous-tags chaotiques |
| **Gambling** | SalesMan, Ricardo |
| **Skill Issue** | C#, Vibecoder, *Are you winning son* |
| **Dark Souls**, **Ez** | GitGud, Pray the Sun |
| **PlantsVsZombie** | Sun Flower |

---

## Effets uniques (sans mot-clé natif)

Quelques cartes ont des mécaniques ad-hoc qui n'ont pas de mot-clé moteur dédié :

- **Charge / attaque immédiate** — *Ruban Blanc des Messagers* permet aux Monstres alliés d'attaquer dès la pose.
- **Pose en chaîne** — *Eileen Conseillère* joue toutes les copies d'une carte ≤ 3 mana du deck et de la main.
- **Transformation d'unité** — chaînes Jonathan (4 formes) et Dio (2 formes) remplacent l'Unit sur le plateau par sa forme suivante.
- **Win conditions conditionnelles** — *Chapeau des Messagers de Yharnam* (toutes les Offrandes Messagers sur terrain), *Tiers de Cordon Ombilical* (3 copies jouées), *Floppa : Divinité* (chaîne complète).

---

## Référence rapide

Pour les règles de combat, de tour, de mana et de plateau, voir [`rules.md`](./rules.md).
Pour les paliers de progression (rangs, Étincelles), voir [`ranked.md`](./ranked.md).
Pour l'économie de collection (packs, fragments, decraft), voir [`economy.md`](./economy.md).
