# Recettes de Nicolas Sagon

Ce depot contient ma collection personnelle de recettes au format Cooklang.

Cooklang est un langage de recette en texte brut (`.cook`) qui permet de garder des recettes lisibles pour les humains et parseables par des outils.

## Structure du projet

- `préparations vegan/` : sauces, bases, preparations
- `recettes vegan/` : plats complets

## Base technique

Le projet est base sur:
- Le format Cooklang: https://cooklang.org/docs/spec/
- L'outil officiel CookCLI: https://cooklang.org/cli/

Le serveur web local est lance avec la commande officielle `cook server`.

## Lancer le serveur web avec Docker

Prerequis:
- Docker Desktop (macOS / Windows) ou Docker Engine + Docker Compose (Linux)

Depuis la racine du projet:

```bash
docker compose up -d
```

Puis ouvrir:
- http://localhost:9080

Arreter le serveur:

```bash
docker compose down
```

## Installation locale CookCLI (sans Docker)

## macOS

Option recommandee (officielle):

```bash
brew install cookcli
```

Puis lancer le serveur depuis ce dossier:

```bash
cook server
```

## Linux

Option simple:
- Telecharger le binaire depuis les releases officielles:
  https://github.com/cooklang/CookCLI/releases

Ensuite, depuis la racine du projet:

```bash
cook server
```

## Windows

Option simple:
- Telecharger `cook.exe` depuis les releases officielles:
  https://github.com/cooklang/CookCLI/releases
- Ajouter le dossier de `cook.exe` au `PATH`.

Puis dans PowerShell, depuis la racine du projet:

```powershell
cook server
```

## Commandes utiles

Afficher une recette:

```bash
cook recipe "recettes vegan/gratin-chou-fleur-vegan.cook"
```

Lancer le serveur sur un port custom:

```bash
cook server --port 8080
```

Autoriser l'acces depuis d'autres appareils du reseau:

```bash
cook server --host
```

## References officielles Cooklang

- Getting Started: https://cooklang.org/docs/getting-started/
- CookCLI: https://cooklang.org/cli/
- CookCLI GitHub: https://github.com/cooklang/CookCLI
