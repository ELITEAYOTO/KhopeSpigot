# KhopeSpigot

KhopeSpigot est un fork personnalisé de [PandaSpigot](https://github.com/hpfxd/PandaSpigot) pour **Minecraft 1.8.8**.

Le projet conserve la base, les optimisations et les correctifs de PandaSpigot tout en ajoutant des modifications spécifiques à KhopeSpigot et aux besoins du serveur **Volkaria**.

> **Upstream principal :** [hpfxd/PandaSpigot](https://github.com/hpfxd/PandaSpigot)

## Objectifs

KhopeSpigot vise principalement à fournir une base 1.8.8 :

- performante ;
- stable ;
- adaptée à un serveur Faction ;
- compatible avec les systèmes spécifiques de Volkaria ;
- facile à maintenir par rapport aux évolutions de PandaSpigot ;
- capable d'accueillir des optimisations et correctifs réseau, chunks, entités et gameplay.

## Base du projet

KhopeSpigot est dérivé de plusieurs projets open source, notamment :

- [PandaSpigot](https://github.com/hpfxd/PandaSpigot) ;
- Paper ;
- Spigot / CraftBukkit.

Une grande partie de l'historique Git du dépôt provient donc de PandaSpigot et de ses projets upstream.

Les contributeurs historiques affichés par GitHub correspondent aux auteurs des commits présents dans cet historique. Leur présence dans la liste des contributeurs ne signifie pas qu'ils participent directement au développement de KhopeSpigot.

## Modifications KhopeSpigot

Les modifications propres à KhopeSpigot sont maintenues au-dessus de la base PandaSpigot.

Le dépôt utilise notamment le système de patches hérité de PandaSpigot :

```text
patches/
```

Lorsque cela est pertinent, les changements apportés aux sources upstream doivent rester aussi isolés et lisibles que possible afin de faciliter les futures mises à jour depuis PandaSpigot.

## Compilation

### Prérequis

Pour compiler KhopeSpigot :

- JDK 17 ;
- Git ;
- Bash.

JDK 17 est utilisé pour le processus de build et de décompilation hérité de PandaSpigot.

### Build

Depuis la racine du dépôt :

```bash
./panda jar
```

Le JAR Paperclip final est généré dans :

```text
paperclip.jar
```

Sous Windows, il est recommandé d'utiliser un environnement Bash compatible, par exemple Git Bash ou WSL, pour les scripts prévus pour Bash.

## Dépôts Git

Le dépôt KhopeSpigot utilise la convention suivante :

```text
origin   -> ELITEAYOTO/KhopeSpigot
upstream -> hpfxd/PandaSpigot
```

Pour récupérer les dernières références PandaSpigot sans modifier la branche de travail :

```bash
git fetch upstream
```

Pour voir les commits présents dans PandaSpigot mais pas encore dans KhopeSpigot :

```bash
git log main..upstream/master --oneline
```

Pour voir les commits propres à KhopeSpigot par rapport à PandaSpigot :

```bash
git log upstream/master..main --oneline
```

Les mises à jour upstream doivent être intégrées volontairement et testées avant d'être ajoutées à `main`.

## Branches

La branche principale de KhopeSpigot est :

```text
main
```

La branche upstream de PandaSpigot reste accessible localement via :

```text
upstream/master
```

## Contributions

Avant toute contribution, consulte [CONTRIBUTING.md](./CONTRIBUTING.md).

Pour l'historique et les crédits des projets dont KhopeSpigot est dérivé, consulte [CREDITS.md](./CREDITS.md).

## Support

KhopeSpigot est un fork indépendant.

Pour les problèmes concernant exclusivement PandaSpigot et non les modifications KhopeSpigot, utilise les ressources officielles du projet PandaSpigot.

## Licence

KhopeSpigot conserve la licence **GNU General Public License v3.0** applicable au projet dont il est dérivé.

Consulte [LICENSE.md](./LICENSE.md) pour le texte complet de la licence.

Les droits d'auteur des portions de code provenant de PandaSpigot, Paper, Spigot et des autres projets upstream restent attribués à leurs auteurs respectifs.
