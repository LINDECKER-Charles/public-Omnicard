# Règles du jeu — Omnicard

> Version joueur des règles du moteur. Pour le glossaire des mots-clés / effets, voir [`keywords.md`](./keywords.md).
> Pour les types de cartes en détail, voir [`card-types.md`](./card-types.md).

---

## 1. Vue d'ensemble

Omnicard est un TCG (trading card game) tour-par-tour à deux joueurs. Chaque joueur incarne un héros à **30 PV**, dispose d'une réserve de **Mana** et d'une mécanique secondaire d'**Extase**, pose des unités sur un **plateau à deux lignes**, joue sorts, équipements, terrains et pièges, et tente de réduire les PV adverses à 0.

### Conditions de victoire

- Réduire les PV de l'adversaire à **0**.
- Déclencher un **effet de victoire automatique** (certaines Légendaires : Chapeau des Messagers, 3 Tiers de Cordon Ombilical joués…).
- L'adversaire abandonne.
- **Match nul** par proposition acceptée ou par effet (ex. la carte WTF *GitGud* force le nul).

---

## 2. Composition d'un deck

Un deck comporte **40 cartes**.

| Statut | Limite par deck |
|---|---|
| **Base** | 3 exemplaires max |
| **Légendaire** | 1 exemplaire max |
| **Invocation** | Jamais directement — uniquement générée par effets, dans un pool dédié |

Certaines cartes ont le mot-clé **Initiale** : si leur condition d'éveil est remplie au moment du build (par exemple « le deck contient ≥ 6 Runes uniques »), elles partent automatiquement en main avant la pioche de départ.

---

## 3. Mise en place de la partie

1. **Brassage** des deux decks.
2. **Tirage** aléatoire du premier joueur (50/50).
3. **Cartes Initiales** — les cartes éligibles partent en main.
4. **Pioche** de départ : chaque joueur complète sa main à **6 cartes**.
5. **Compensation second joueur** : il reçoit **+1 Mana max permanent**. Son tour 1 commence donc à 4 mana max (vs 3 pour le premier joueur, qui a déjà bénéficié de l'incrément automatique du début de son tour).
6. **Mulligan** — chaque joueur peut renvoyer jusqu'à 5 cartes et repiocher autant. La partie ne démarre que quand les deux ont résolu.

---

## 4. Structure d'un tour

### Début de tour du joueur actif

1. **Pioche** d'1 carte.
2. **Toutes les unités** sur ton plateau deviennent *Prêtes à attaquer*.
3. **Ressources** :
   - Les manas non utilisés au tour précédent sont **convertis en Cristaux** (plafond 5).
   - Mana courante remise à 0, mana max +1 (plafond 10), puis mana courante remplie au max.

### Pendant ton tour

Tu peux enchaîner librement :

- **Jouer une carte** (Unit / Spell / Gear / Ground / Trap).
- **Attaquer** avec n'importe quelle unité *Prête à attaquer*.
- **Activer un Gear** qui expose un effet activable.
- **Résoudre un choix en attente** (modal ouvert par certains effets — Jojo Pose, Stockage).
- **Proposer un match nul** ou y répondre.
- **Abandonner**.
- **Terminer ton tour**.

### Fin de tour

- Tous les **effets de fin de tour** de tes unités et de ton Terrain se déclenchent.
- Les **effets différés** voient leur compteur décrémenter ; à 0, ils s'exécutent. Si l'unité qui les a programmés est morte, l'effet est annulé.
- Tour suivant pour l'adversaire.

---

## 5. Ressources

### Mana et Cristaux

| Ressource | Initial | Plafond | Notes |
|---|---:|---:|---|
| **Mana courante** | 0 | = Mana max | Remplie à chaque début de tour |
| **Mana max** | 2 | 10 | +1 chaque début de tour, +1 permanent pour le 2ᵉ joueur |
| **Cristaux** | 0 | 5 | Réserve persistante. Alimentée par la mana non dépensée. Consommée après la mana courante |

Le **total dépensable** = Mana courante + Cristaux. À l'achat d'une carte, la mana courante est consommée d'abord, puis les cristaux complètent.

### Points de vie

- Démarre à 30 PV / 30 PV max.
- Le max peut bouger (cartes Métamorphose Horaire / Antihoraire) ; les PV courants sont reclampés à la baisse si nécessaire.
- À 0 PV, la partie est perdue.

### Extase

Ressource secondaire alimentée par **les dégâts**.

| Aspect | Règle |
|---|---|
| Gain | +1 par point de dégât infligé (l'inflicteur gagne, même contre sa propre unité ou son propre héros) |
| Multiplicateur | *Le Rêve du Chasseur* double les gains tant qu'il est sur le terrain |
| Consommation | Coûts custom de certaines cartes (Communion, Vision, Bête Crucifier, Yharnam : Centre…) |
| Seuils | Certains effets se déclenchent à *Extase ≥ N* sans dépense (Atelier des Gemmes à 30, Lame Sépulcrale à 15…) |
| Compteur cumulé | L'Extase gagnée à vie ne se réinitialise jamais (utilisée par certains effets) |

---

## 6. Plateau

| Zone | Capacité | Notes |
|---|---|---|
| **Front Line** | 10 unités | Cible directement adverse |
| **Back Line** | 10 unités | Cible directement adverse |
| **Cimetière** | ∞ | Cartes consommées (sauf Abyssal) |
| **Pièges** | ∞ | Cartes face cachée |
| **Terrain** | 1 seul | Un nouveau Terrain remplace l'ancien |

- **Toute unité peut attaquer n'importe quelle unité ennemie**, modulo les règles de ciblage (cf. Provocation).
- Le **héros adverse n'est attaquable que si son plateau est vide**.
- **Main maximale** : 10 cartes. En cas d'overflow, la carte excédentaire part au cimetière par défaut.

---

## 7. Combat

### Initier une attaque

L'attaquant doit être :
- À toi ;
- *Prêt à attaquer* (en général posé au tour précédent, sauf effets de Charge) ;
- Choisi pendant ton tour, partie en cours.

### Règles de ciblage

1. La cible doit être adverse.
2. **Provocation prioritaire** — s'il y a au moins une unité ennemie avec Provocation, tu **dois** la cibler en premier. Sinon, n'importe laquelle.
3. **Héros attaquable uniquement si plateau adverse vide.**

### Résolution d'une attaque

Dégâts infligés = Attaque de l'attaquant (+ Attaque du Gear porté s'il y en a un).

Côté cible, la mitigation s'applique **dans cet ordre** :

1. **Esquive(N)** — consomme 1 stack, annule entièrement la frappe.
2. **Règle spéciale d'incoming** — certaines cartes ont leur propre logique (ex. Floppa : Guerrier divise par 2 si PV > 10).
3. **Robustesse(N)** — soustrait N points fixes (clampé à 0).
4. **Gear en priorité** — les PV de l'équipement absorbent en premier, le reliquat tape sur l'unité.

Si la cible meurt, elle va au cimetière (avec son Gear et toutes ses incrustations).

**Riposte** — la cible riposte de sa propre Attaque, sauf si :
- C'est le héros (le héros ne riposte jamais).
- Une règle spéciale annule la riposte (ex. Floppa : Assassin).

L'attaquant passe à *non Prêt à attaquer* après son attaque.

### Soins

Soigne d'abord le **Gear** s'il est endommagé, puis l'unité. Les bonus de soin de certaines cartes (Communion) s'appliquent avant le clamp.

---

## 8. Jouer une carte

### Conditions

- Phase et tour valides ;
- Carte présente en main ;
- Mana totale ≥ coût actuel de la carte ;
- Pour une Unit, ligne ciblée non pleine ;
- Pour un Gear, cible valide (unité ou Gear principal à incruster) ;
- Pour un Sort ciblé sur une unité avec **Anti-Magie**, le sort est bloqué.

### Coût d'une carte

Le coût final est calculé dynamiquement :

1. **Override temporaire** prioritaire si une carte t'en donne un.
2. **Coût de base** de la carte, parfois modulé par condition (ex. Communion +4 coûte 0 si les 3 précédents Communion sont au cimetière).
3. **Discount additifs** — réductions accumulées :
   - Sur la prochaine carte (one-shot, Vision +1).
   - Sur tous les Gear (Festival d'Urnes).
   - Sur tous les Pièges (Œdon Impalpable).
   - Sur la famille Grand (Mergot).
   - Sur la famille Ésotérisme (Gemme: Triangle 2 si Extase ≥ 10).
   - Sur la famille Offrande (Vasque : Lucidité).
   - Sur les Gear Outil ∧ Chasseur (Atelier des Armes).
4. **Clamp final à 0**.

### Paiements custom

Certaines cartes consomment **mana + Extase** au lieu de mana seule :
- Communion +2, Vision +2 — *Extase → X* (tu saisis X variable).
- Communion +3 — *Extase(10)* fixe en plus du mana.
- Yharnam : Centre — mana réduite par l'Extase courante.

Si l'un des paiements échoue, l'autre est restitué et la pose est annulée.

### Équipement et incrustation

- Un **Gear** s'équipe sur **une unité**.
- Un Gear avec le mot-clé **Incrustation** (les Gemmes Bloodborne) peut être :
  - Incrusté sur un Gear existant (max 3 incrustations par Gear) ;
  - Ou équipé seul comme Gear principal si l'unité n'a pas de Gear.
- Si tu remplaces le Gear principal d'une unité, l'ancien Gear + ses incrustations retournent en main.
- À la mort de l'unité, Gear et incrustations partent au cimetière.

### Pièges

- Posés faces cachées (l'adversaire **ne voit pas** la carte à la pose).
- Effet persistant actif tant que dans la zone Pièges.
- À l'activation : retirés de la zone, envoyés au cimetière, **révélés aux deux joueurs**.

### Choix en attente

Certaines cartes (Jojo Pose, Stockage) piochent N cartes et ouvrent un **modal de sélection**. Tu choisis lesquelles jouer et dans quel ordre — les non-sélectionnées partent au cimetière.

---

## 9. Effets de cartes — comment ils s'activent

Le moteur émet des événements à chaque transition importante (carte jouée, unité morte, dégâts subis, Extase gagnée, mana dépensée, début de tour…). Les **effets persistants** s'abonnent à ces événements.

Un effet persistant est attaché quand sa carte source entre dans son slot (board, terrain, gear équipé, piège posé, sort au cimetière) et détaché à la sortie.

Pour le détail des mots-clés et de leurs triggers, voir [`keywords.md`](./keywords.md).

---

## 10. Effets différés

Certaines cartes programment un effet pour **plusieurs tours plus tard** — par exemple *Floppa : Divinité* fait 100 dégâts à l'adversaire 2 tours après sa pose.

- Le compteur décrémente uniquement à la fin du tour du joueur qui a programmé l'effet.
- Si l'unité qui a programmé l'effet meurt, l'effet est annulé.
- Un décompte visuel s'affiche sur l'unité concernée.

---

## 11. Buffs globaux par famille

Certaines cartes buffent **toutes les copies d'une famille** chez le joueur (en main, dans le deck, au cimetière, sur le plateau).

Exemples :
- *Lune Sanglante* — +1/+0 à toute la famille Grand.
- *Cerveau de Mensis* — +3/+3 à toute la famille Grand (effet différé 4 tours).
- *Communion +4* — +2/+2 à toute la famille Chasseur.

Ces buffs sont visibles dans le HUD du joueur.

---

## 12. Fin de partie

| Cause | Effet |
|---|---|
| PV ≤ 0 d'un joueur | L'autre gagne |
| Abandon | L'autre gagne |
| Match nul accepté | Égalité, pas de vainqueur |
| Match nul forcé (GitGud) | Idem |
| Effet de victoire automatique d'une carte | Le détenteur de l'effet gagne |

---

## 13. Limites du moteur

| Limite | Valeur |
|---|---:|
| PV initiaux | 30 |
| Main maximale | 10 cartes |
| Mana max plafond | 10 |
| Cristaux plafond | 5 |
| Front Line max | 10 unités |
| Back Line max | 10 unités |
| Mulligan max | 5 cartes |
| Incrustations max par Gear | 3 |
| Pioche de départ | 6 cartes |
| Compensation 2ᵉ joueur | +1 Mana max |
