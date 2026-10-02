# RisoExpert Suite

Ce dépôt central relie les quatre projets RisoExpert sans dupliquer leurs sources.
Chaque projet reste autonome, avec son propre historique GitHub et son cycle de publication.

| Projet | Responsabilité | Dépôt source |
| --- | --- | --- |
| `apps/public-site` | Site public officiel et demandes clients | `risoexpert-public-site` |
| `apps/platform` | Plateforme métier, applications mobile et web | `risoexpert-platform` |
| `apps/admin` | Administration web actuellement distribuée | `risoexpert-admin` |
| `apps/next` | Nouvelle vitrine RisoExpert publiée | `risoexpert-next` |

## Utilisation

Clonez l’ensemble avec les sous-modules :

```sh
git clone --recurse-submodules https://github.com/nikaisedoua-source/risoexpert-suite.git
```

Après un clone normal, initialisez-les avec :

```sh
git submodule update --init --recursive
```

## Règle d’architecture

Les quatre projets sont connectés par ce dépôt de coordination, mais aucun code n’est fusionné automatiquement. Les changements applicatifs doivent être effectués dans le sous-module concerné, testés, puis poussés dans son dépôt d’origine. Le dépôt `risoexpert-suite` enregistre ensuite la révision validée de chaque application.

Cette séparation évite qu’une mise à jour du site vitrine perturbe la plateforme métier ou l’administration.
