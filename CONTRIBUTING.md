# Contribuer à KhopeSpigot

Merci de vouloir contribuer à KhopeSpigot.

KhopeSpigot étant basé sur PandaSpigot et sur son système de patches, les modifications doivent rester aussi propres, isolées et faciles à maintenir que possible.

## Avant de modifier le code

Travaille toujours depuis une branche créée à partir de la version actuelle de `main`.

Exemple :

```bash
git switch main
git pull
git switch -c feature/nom-de-la-modification
```

Évite de travailler directement sur `main` pour les changements importants.

## Modifications des sources upstream

Lorsqu'un fichier provenant directement de PandaSpigot, Paper ou Spigot est modifié :

- garde le diff aussi petit que possible ;
- évite les changements de formatage inutiles ;
- respecte le style du code environnant ;
- documente les changements qui ne sont pas évidents ;
- vérifie que le changement ne casse pas la compatibilité avec les plugins 1.8.8.

Les modifications doivent rester compatibles avec le système de patches utilisé par le projet.

## Organisation des commits

Un commit doit idéalement correspondre à une modification logique.

Préférer :

```text
Fix chunk packet visibility
Optimize entity tracker flush
Add configurable mining tick delay
```

Éviter :

```text
update
fix
test
changes
```

Les commits doivent permettre de comprendre rapidement ce qui a été changé et pourquoi.

## Avant un commit

Vérifie toujours l'état du dépôt :

```bash
git status
```

Puis inspecte les changements :

```bash
git diff
```

Ajoute ensuite uniquement les fichiers voulus :

```bash
git add <fichier>
```

ou, lorsque tous les changements sont volontairement inclus :

```bash
git add .
```

Enfin :

```bash
git commit -m "Description claire du changement"
```

## Tests

Avant de pousser un changement important :

- vérifie que le projet compile ;
- vérifie que les patches s'appliquent correctement ;
- teste les modifications concernées sur un environnement serveur adapté ;
- surveille les erreurs console et les régressions de compatibilité.

Build principal :

```bash
./panda jar
```

## Synchronisation avec PandaSpigot

Le dépôt original PandaSpigot est configuré localement sous le remote :

```text
upstream
```

Pour récupérer son état récent :

```bash
git fetch upstream
```

Cette commande ne modifie pas automatiquement `main`.

Ne fusionne pas aveuglément `upstream/master` dans `main`. Les changements upstream doivent être examinés, intégrés et testés volontairement.

## Pull Requests

Une Pull Request doit expliquer au minimum :

- le problème ou l'objectif ;
- les fichiers ou systèmes concernés ;
- le comportement avant la modification ;
- le comportement après la modification ;
- les tests effectués ;
- les éventuels risques ou effets secondaires.

## Compatibilité

KhopeSpigot cible Minecraft 1.8.8.

La compatibilité avec les plugins existants est importante. Toute modification de comportement Bukkit, Spigot, Paper ou PandaSpigot doit être considérée avec prudence.

## Sécurité

Ne commit jamais :

- mots de passe ;
- tokens GitHub ;
- clés API ;
- identifiants de base de données ;
- fichiers de configuration contenant des secrets ;
- données privées provenant d'un serveur de production.

Si un secret a été commit par erreur, le supprimer du fichier ne suffit pas nécessairement : il doit également être révoqué et, si nécessaire, retiré de l'historique Git.

## Licence

Toute contribution à KhopeSpigot doit être compatible avec la licence GPL-3.0 du projet.
