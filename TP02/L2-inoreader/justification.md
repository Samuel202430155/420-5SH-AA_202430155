# L2 — Justification du système Inoreader

**DA : 202430155 — Date : 2026-10-09**

## Dossiers (4)

- **A1-Automatisation-TI** : automatisation de l'infrastructure et des workflows TI — communautés r/sysadmin et r/devops, Mastodon Hachyderm (infra/SRE), r/hashicorp (Terraform), blogues OpenTofu et Red Hat. Alerte Google A1 en RSS.
- **A2 — CI/CD & pipelines** : CI/CD déclaratif et pipelines programmables — blogues Azure DevOps, GitLab (Major Releases), GitHub, CircleCI, JFrog, chaîne YouTube CNCF (KubeCon, Kyverno, eBPF). Alerte Google A2 en RSS.
- **A3 — Dagger** : moteur CI/CD as code ciblé — releases GitHub `dagger/dagger`, commits du dépôt `dagger/dagger`, r/selfhosted, releases Kubernetes (écosystème cloud native auquel Dagger s'intègre). Alerte Google A3 en RSS.
- **Stratégique** : rapports annuels et sectoriels (DORA State of DevOps, InfoQ, Stack Overflow Blog, The New Stack) — séparés des flux quotidiens car lus à un autre rythme (mensuel).

## Étiquettes (4 minimum) et leur logique

| Étiquette | Sens |
|---|---|
| `à-tester` | Techno à essayer si l'occasion se présente (signal fort sur un outil) |
| `signal-faible` | Émergence à surveiller, rien de concluant encore |
| `pour-le-carnet` | À traiter dans l'entrée de la semaine |
| `sécurité` | Vulnérabilité ou avis touchant un de mes axes (priorité) |

## Traitement hebdomadaire du flux

1. **Quotidien (10 min, 8h15)** : parcourir les dossiers A1–A3, étiqueter, marquer le reste comme lu (règle des 2 minutes).
2. **Hebdo (jeudi 19h, 30 min)** : lire les articles `pour-le-carnet`, rédiger l'entrée S__ dans `carnet/`, committer.
3. **Mensuel (1er lundi)** : dossier `Stratégique`, revue des sources bruyantes, désabonnements.

## Compteurs exigés (à compléter)

- Feuilles de route : 20 flux RSS accessibles (4 dossiers), dont 2 flux releases GitHub (`dagger/dagger` et `kubernetes/kubernetes`), 3 flux réseaux sociaux / communautés (r/devops, r/sysadmin, r/selfhosted) + Mastodon Hachyderm et YouTube CNCF, 3 alertes Google en flux RSS, 1 infolettre.
- Export OPML : `Inoreader Feeds 20261009.xml` (dans `captures/`)
- Captures : 4 à 6 dans `captures/` (arborescence des dossiers, page d'un flux, gestion des étiquettes, articles sauvegardés)

> **Bonus (+3)** : règles / filtres / flux de surveillance Inoreader Pro (essai 15 jours) — documentés ici si configurés (règle, condition, action, effet observé).