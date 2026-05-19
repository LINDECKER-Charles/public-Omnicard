# Contribuer à Omnicard

Merci de t'intéresser au projet. Voici comment participer concrètement.

## Avant tout

Lis [`LEGAL.md`](./LEGAL.md) et [`legal/charte-de-conduite.md`](./legal/charte-de-conduite.md). Omnicard est un fan-project non commercial — toute contribution doit respecter ce cadre.

## Proposer une carte

Deux canaux :

- **GitHub Issue** avec le template `Proposition de carte` (formaté, permanent, traçable).
- **Discord** ([discord.gg/XBY9FPNv9g](https://discord.gg/XBY9FPNv9g)) — salon `Suggestions`, plus rapide pour itérer.

Format imposé : voir le template d'Issue ou le guide du forum Discord.

## Signaler un bug

Via les **Issues** avec le template `Bug`. Précise toujours :

- la plateforme (prod `omnicard.fr` / test `test.omnicard.fr`) ;
- la façon de reproduire ;
- le navigateur et la date approximative.

## Poser une question sur une règle

Via les **Discussions** (catégorie `Questions règles`), pas les Issues. La réponse marquée comme officielle finit dans la FAQ.

## Soumettre une Pull Request

Pour les modifications de documentation (typos, clarifications, ajouts dans `docs/`) :

1. Fork le dépôt.
2. Crée une branche descriptive (`docs/corrige-regle-mana`).
3. Commit avec un message clair (voir ci-dessous).
4. Ouvre la PR avec une description du changement.

Pour le **contenu de cartes** (ajout d'une carte ou modification d'effet) : **discute d'abord** sur Discord ou via une Issue. On évite les PR de contenu non concertées — l'équilibrage est trop dépendant du reste du moteur.

## Format des messages de commit

```
type: résumé court (impératif, ≤ 70 caractères)

Description plus détaillée si besoin (paragraphe optionnel).
```

Types acceptés : `docs`, `rules`, `card`, `fix`, `refonte`.

## Code de conduite

Reste respectueux. Le tag WTF est un permis de délire, pas un permis de toxicité. Pas de contenu haineux, pas de harcèlement, pas de spam.

Tout abus mène à un ban du dépôt et du Discord. Détails : [`legal/charte-de-conduite.md`](./legal/charte-de-conduite.md).

## Reconnaissance

Les contributions intégrées au jeu sont mentionnées dans le [`CHANGELOG.md`](./CHANGELOG.md) à chaque release pertinente.
