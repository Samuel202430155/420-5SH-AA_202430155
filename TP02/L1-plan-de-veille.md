# Plan de veille — L1
**420-5SH-AA — Veille et intégration technologique**  
**Étudiant :** Samuel LAWSON HETCHELY —  
**DA :** 202430155  
**Date :** 2026-09-21

---

## Vue d'ensemble

| Axe | Portée | Types de veille mobilisés |
|---|---|---|
| A1 — Automatisation de l'infrastructure et des workflows TI | Large | Sectorielle, stratégique, réseaux sociaux |
| A2 — CI/CD déclaratif et pipelines programmables | Moyenne | Sectorielle, réseaux sociaux, concurrentielle |
| A3 — Dagger (moteur de CI/CD as code) | Ciblée | Sectorielle, réseaux sociaux, concurrentielle |

Les trois axes forment un entonnoir : A1 donne le contexte général de l'automatisation pour une petite équipe TI, A2 creuse l'angle précis des pipelines de livraison, et A3 évalue un outil concret qui s'inscrit directement dans A2. Ils se nourrissent l'un l'autre : une nouvelle capacité de Dagger se lit d'abord comme un événement du domaine A2, puis comme un signal d'adoption dans le contexte A1.

---

## Axe 1 — Automatisation de l'infrastructure et des workflows TI

**Objectif**
Identifier les pratiques d'automatisation (infrastructure as code, scripts, orchestration) adaptées à une PME de 40 employés dont l'équipe TI compte quatre personnes, afin de réduire les tâches répétitives et les erreurs manuelles.

**Questions de veille**
1. Quels scénarios d'automatisation sont les plus rentables pour une petite équipe TI (provisionnement, mises à jour de parc, sauvegardes, intégration d'un nouvel employé) ?
2. Quelle place occupent les pratiques « as code » (infrastructure, configuration, politiques) en 2026 dans les organisations de petite taille ?
3. Quels outils (Ansible, OpenTofu, scripts, orchestration) les PME utilisent-elles réellement, par opposition à ce que le marketing des éditeurs recommande ?

**Mots-clés**
automatisation TI, infrastructure as code, IaC, orchestration, provisionnement, gestion de parc, runbook, Ansible

**Requête booléenne (Google Alerts → RSS)**
`("IT automation" OR "infrastructure as code" OR IaC) AND (Ansible OR "small team" OR runbook) -cours -formation`

**Types de veille**
Sectorielle (état des pratiques) · Stratégique (rapports annuels DORA) · Réseaux sociaux et communautés (retours terrain)

**Sources ciblées**

| Source | Type de source | Fréquence |
|---|---|---|
| Documentation officielle Ansible — blogue | Documentation officielle | Hebdomadaire |
| Blogue OpenTofu / HashiCorp — infrastructure as code | Blogue officiel | Hebdomadaire |
| r/devops, r/sysadmin | Communauté | Hebdomadaire |
| Compte Mastodon d'un praticien de l'automatisation infra | Réseau social professionnel | Quotidien |
| Rapport annuel DORA « State of DevOps » | Rapport sectoriel | Annuel (dossier `Stratégique`) |
| Alerte Google — requête ci-dessus | Alerte agrégée | Quotidien |

---

## Axe 2 — CI/CD déclaratif et pipelines programmables

**Objectif**
Déterminer comment rendre les pipelines de build, test et déploiement de l'équipe déclaratifs, testables et réutilisables, sans multiplier les outils ni verrouiller l'équipe sur un fournisseur.

**Questions de veille**
1. Quels sont les forces et limites actuelles des approches déclaratives (GitHub Actions, GitLab CI, Tekton) par rapport aux pipelines programmables (Dagger) ?
2. Comment tester la logique d'un pipeline localement avant de le pousser en production ?
3. Que rapportent les équipes qui ont migré un pipeline YAML vers une version « as code », et celles qui sont revenues en arrière ?

**Mots-clés**
CI/CD, pipeline as code, GitHub Actions, GitLab CI, Tekton, test de pipeline, Dagger

**Requête booléenne (Google Alerts → RSS)**
`(CI/CD OR "pipeline as code") AND (GitHub Actions OR GitLab OR Tekton OR Dagger) -formation -certification`

**Types de veille**
Sectorielle · Réseaux sociaux et communautés · Concurrentielle (comparaison des plateformes CI/CD)

**Sources ciblées**

| Source | Type de source | Fréquence |
|---|---|---|
| GitHub — changelog et documentation Actions | Documentation officielle | Quotidien |
| Blogue CI/CD de GitLab | Blogue officiel | Hebdomadaire |
| r/devops | Communauté | Hebdomadaire |
| Offres d'emploi mentionnant les pipelines (LinkedIn, Indeed) | Veille concurrentielle (adoption réelle) | Mensuel |
| Talks de conférences CI/CD sur YouTube | Vidéo technique | Hebdomadaire |

---

## Axe 3 — Dagger (moteur de CI/CD as code)

**Objectif**
Évaluer si Dagger — qui permet d'écrire ses pipelines en code (Go, Python, TypeScript) et de les exécuter par conteneurs — est adapté pour standardiser les pipelines d'une équipe de quatre développeurs, ou s'il est préférable de rester sur une plateforme configurée en YAML (GitHub Actions).

**Questions de veille**
1. Quelle est la maturité de Dagger en 2026 (versions stables, adoption, cas d'usage documentés) ?
2. Quels sont les retours concrets des équipes qui l'ont adopté — et surtout de celles qui ont fait marche arrière ?
3. Quelle est la courbe d'apprentissage pour une équipe qui maîtrise déjà GitHub Actions ?

**Mots-clés**
Dagger, dagger.io, CI/CD as code, pipeline programmable, SDK Go/Python/TypeScript

**Requête booléenne (Google Alerts → RSS)**
`(Dagger OR "dagger.io") AND (CI/CD OR pipeline OR "production" OR "self-hosted") -jeu -épée`

**Types de veille**
Sectorielle · Réseaux sociaux et communautés (Discord Dagger, r/devops) · Concurrentielle (vs GitHub Actions, Tekton)

**Sources ciblées**

| Source | Type de source | Fréquence |
|---|---|---|
| Releases GitHub de `dagger/dagger` | Source primaire | Au fil des versions |
| Blogue officiel Dagger — dagger.io/blog | Blogue officiel (éditeur intéressé) | Hebdomadaire |
| Communauté Discord Dagger | Communauté | Au besoin |
| Chaîne YouTube de conférences CI/CD | Vidéo technique | Hebdomadaire |
| Offres d'emploi mentionnant Dagger (LinkedIn, Indeed) | Veille concurrentielle | Mensuel |

> Note : Dagger figure dans l'anneau TRIAL du ThoughtWorks Technology Radar. La source est conservée car le produit est ouvert (open source) et publie des informations techniques détaillées, mais le critère *Purpose* de sa fiche CRAAP devra être vérifié (éditeur qui vend son produit).

---

## Ma routine de veille

| Fréquence | Durée | Quand exactement | Quoi |
|---|---|---|---|
| Quotidien | 10 min | Lundi au vendredi, 17 h 45 | Parcourir Inoreader, étiqueter, marquer le reste comme lu |
| Hebdomadaire | 30 min | Samedi, 10 h | Lire les articles étiquetés `pour-le-carnet`, rédiger l'entrée de la semaine |
| Mensuel | 45 min | Dernier dimanche du mois, 19 h | Dossier `Stratégique`, révision des sources, désabonnements |

---

## Schéma de mon système

```
   SOURCES PUSH                    SOURCES PULL
   ─────────────                   ─────────────
   Flux RSS (blogues, docs)        DORA State of DevOps
   Alertes Google (3)              Offres d'emploi (mensuel)
   Releases GitHub (dagger, …)     Talks conférences CI/CD
   Infolettre                      Rapports Tech Radar (annuel)
   Reddit, Discord, Mastodon, YouTube
           │                              │
           └──────────────┬───────────────┘
                          ▼
                  ┌───────────────┐
                  │   INOREADER   │   4 dossiers, 4 étiquettes
                  └───────────────┘
                          │
                  étiquetage quotidien
                          ▼
                  ┌───────────────┐
                  │    CARNET     │   1 entrée / semaine
                  └───────────────┘
                          │
                          ▼
              ACTION : surveiller · tester ·
              partager · écarter · recommander
```

---

## Mes indicateurs

| Indicateur | Cible | Ce qu'il révèle si la cible n'est pas atteinte |
|---|---|---|
| Articles étiquetés / articles parcourus | Entre 5 % et 12 % | Sous 5 % : mes sources sont mal choisies. Au-dessus de 12 % : je ne trie pas assez sévèrement. |
| Entrées de carnet | 1 par semaine, sans exception | Ma routine ne tient pas ; il faut déplacer le créneau, pas m'en vouloir. |
| Sources ayant produit au moins une entrée | Au moins 9 sur 20 d'ici la semaine 10 | Les autres sont du bruit et devraient être coupées. |
| Signaux faibles repérés | Au moins 3 sur l'ensemble | Je ne lis que des sources grand public qui se reprennent les unes les autres. |

