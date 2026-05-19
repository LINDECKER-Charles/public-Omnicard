# Types de carte

5 types de cartes, chacun avec son rôle et ses règles propres.

---

## Unité

**Créature posée sur le plateau** qui attaque et encaisse.

- A des **PV** et une **Attaque**.
- Posée sur une des 2 lignes (Front Line / Back Line), 10 emplacements par ligne.
- Devient **Prête à attaquer** au tour suivant sa pose (sauf effet de Charge spécifique).
- Peut porter un **Gear** (équipement).
- Va au **cimetière** à sa mort (avec son Gear et ses incrustations).

Les Unités sont le cœur du jeu — elles défendent ton héros, attaquent l'adversaire, et portent la plupart des effets persistants.

## Sort

**Effet immédiat** à usage unique.

- Coût en mana, parfois en Extase.
- Effet résolu à la pose, puis envoi au **cimetière** (sauf attribut spécial).
- Bloqué par **Anti-Magie** s'il cible une unité protégée.
- Certains sorts au cimetière portent un **effet persistant** (ex. Communion +1, Atelier des Gemmes).
- Variante **Réutilisable(N)** : la carte retourne en main au lieu d'aller au cimetière, N fois.
- Variante **Abyssal** : ne va jamais au cimetière, silencieusement détruite après usage.

Les Sorts permettent des effets ponctuels (dégâts directs, soins, pioche, contrôle).

## Gear

**Équipement** attaché à une unité.

- Ajoute son Attaque et ses PV à ceux de l'unité porteuse.
- **Encaisse les dégâts en priorité** sur l'unité (les PV du Gear absorbent avant ceux de l'unité).
- Si le porteur change de Gear, l'ancien Gear retourne en main.
- À la mort de l'unité, le Gear part au cimetière avec elle.
- Certains Gear ont un **effet activable** (ex. interface qui expose une action manuelle).

### Incrustation

Un Gear avec le mot-clé **Incrustation** (les Gemmes Bloodborne notamment) peut être :

- **Incrusté** sur un Gear principal existant — jusqu'à **3 incrustations max** par Gear.
- **Équipé seul** comme Gear principal si l'unité n'en a pas.

Les stats des incrustations s'additionnent à celles du Gear porteur.

## Terrain (Ground)

**Carte de zone unique** qui modifie les règles globales tant qu'elle est en jeu.

- **1 seul Terrain actif** par joueur. Un nouveau Terrain remplace l'ancien.
- Peut avoir un **effet de fin de tour** (ex. *L'Atelier du Chasseur* applique Affûtage(1,1) à tous les Gears).
- Peut avoir un **effet persistant** (ex. *Le Rêve du Chasseur* double les gains d'Extase).
- Pas de stats (ni PV ni Attaque), pas attaquable.

## Piège

**Carte posée face cachée** qui se déclenche selon une condition adverse.

- L'adversaire **ne voit pas** la carte à la pose.
- Effet **persistant** souscrit à un événement (attaque, pose adverse, fin de tour, etc.).
- Au déclenchement : retiré de la zone Pièges, **révélé aux deux joueurs**, envoyé au cimetière.
- Pas attaquable.

---

## Tableau récapitulatif

| Type | Stats | Zone destination | Cible adversaire ? |
|---|---|---|---|
| **Unité** | PV + Attaque | Plateau → cimetière à la mort | Oui (avec règles de Provocation) |
| **Sort** | — | Cimetière (sauf Abyssal) | Selon le sort |
| **Gear** | PV + Attaque (additifs) | Sur l'unité → cimetière | Cible une unité (alliée ou ennemie selon le Gear) |
| **Terrain** | — | Zone Terrain (1 seul) | Effet de zone |
| **Piège** | — | Zone Pièges → cimetière à l'activation | Réagit à une action adverse |

---

Pour les effets et mots-clés associés à chaque type, voir [`keywords.md`](./keywords.md).
Pour la composition d'un deck, voir [`deck-building.md`](./deck-building.md).
