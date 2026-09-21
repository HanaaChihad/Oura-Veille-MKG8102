# Grille de fiabilité des sources

Équipe 3, MKG8102. Grille conçue par Philippe Gariépy, Responsable des insights jusqu'au 11 septembre 2026, à partir des trois critères de la lecture préparatoire (Fleisher et Bensoussan, 2015). Les lettres reprennent le code de l'Amirauté employé par l'OTAN (doctrine AJP-2.1). Appliquée aux quinze sources de la base le 17 septembre 2026 par la Direction, qui cumule depuis le rôle d'insights.

La lettre qualifie la **source**. La crédibilité de chaque **information** se note séparément, sur la fiche (voir `fiche-de-veille/SKILL.md`). Le niveau de confiance se déduit des deux.

## 1. Trois critères, chacun noté 0, 1 ou 2

| Critère | 2 | 1 | 0 |
|---|---|---|---|
| Proximité (P) | Émettrice : la source produit elle-même l'information (l'acteur pour sa propre offre, le détaillant pour son prix affiché, l'organisme de réglementation pour ses décisions) | Relais qui nomme l'émetteur ou renvoie à sa page | Relais qui ne dit pas d'où vient l'information, ou reprise d'un communiqué sans le signaler |
| Indépendance (I) | La source n'a aucun intérêt dans le contenu | Intérêt déclaré ou évident : marque, détaillant qui vend le produit, affiliation signalée | Intérêt caché : commandite ou affiliation non signalée |
| Historique d'exactitude (H) | Établi : un émetteur identifié répond de ce qu'il publie, ou deux vérifications au registre ont confirmé la source | Non établi : personne ne répond du contenu | Entaché : au moins une erreur inscrite au registre et non corrigée |

## 2. Passage de la somme à la cote

| P + I + H | Cote (valeur Airtable) | Règle d'usage |
|---|---|---|
| 6 | A — Entièrement fiable | Fait foi seule ; référence pour recouper le reste |
| 5 | B — Habituellement fiable | Peut confirmer seule une autre source ; suffit seule pour un seuil d'alerte |
| 3-4 | C — Assez fiable | À recouper par une deuxième source indépendante avant d'appuyer une conclusion ou de déclencher une alerte |
| 2 | D — Peu fiable | Ne suffit jamais seule ; ne déclenche jamais d'alerte ; nourrit le contexte du brief |
| 0-1 | E — Non fiable | Retirée de la liste des sources |
| — | F — Impossible à évaluer | On ne sait pas qui publie ; traitée comme D après deux vérifications |

Une cote basse n'écarte pas une source : elle impose le recoupement. On écarte l'invérifiable, jamais l'orienté. Une source orientée mais identifiée ne descend pas à E : un intérêt déclaré coûte un point (I = 1), pas trois. E ne regroupe que l'invérifiable, c'est pourquoi c'est la seule cote qui retire une source.

## 3. Application aux quinze sources de la base (état au 21 septembre 2026)

Relevé depuis la table Sources d'Airtable (champs Proximité P, Indépendance I, Historique H, Fiabilité). Le biais de chaque source est écrit dans le champ Biais connu.

| Source | Type | P | I | H | Total | Cote | État |
|---|---|---|---|---|---|---|---|
| Santé Canada - registre MDALL | Primaire | 2 | 2 | 2 | 6 | A | Active |
| Best Buy Canada - bagues connectées | Primaire | 2 | 1 | 2 | 5 | B | Active |
| Amazon.ca - bagues connectées | Primaire | 2 | 1 | 2 | 5 | B | À vérifier |
| MobiHealthNews - homologation FDA Samsung | Secondaire | 1 | 2 | 2 | 5 | B | Active |
| RingConn Gen 3 - page produit | Primaire | 2 | 1 | 1 | 4 | C | Active |
| Ultrahuman Ring AIR - page de prix | Primaire | 2 | 1 | 1 | 4 | C | Active |
| Samsung Galaxy Ring Canada - page produit | Primaire | 2 | 1 | 1 | 4 | C | Active |
| Femometer Ring Gen2 - page produit | Primaire | 2 | 1 | 1 | 4 | C | Active |
| Evie Ring - page produit | Primaire | 2 | 1 | 1 | 4 | C | À vérifier |
| Peri (IdentifyHer) - page produit | Primaire | 2 | 1 | 1 | 4 | C | Active |
| Whoop - page produit | Primaire | 2 | 1 | 1 | 4 | C | Active |
| Benefits Canada - ménopause en milieu de travail | Secondaire | 1 | 2 | 1 | 4 | C | Active |
| Wareable - comparatif des bagues connectées 2026 | Secondaire | 1 | 1 | 1 | 3 | C | Active |
| Trustpilot - RingConn | Secondaire | 0 | 1 | 1 | 2 | D | À vérifier |
| Peri (IdentifyHer) - communiqué de lancement | Primaire | — | — | — | — | — | Écartée : adresse morte (19 septembre) |

## 4. Ce que la grille ne fait pas

- Elle ne juge pas une information : une source A peut publier une information non confirmée, une source C une information confirmée ailleurs. C'est le rôle de la crédibilité, sur la fiche.
- Elle ne calcule pas seule. La table Sources propose une cote par un champ calculé (« Cote proposée »), mais la cote qui fait foi est celle qu'un humain inscrit dans le champ Fiabilité. Le champ calculé a un défaut connu, décrit dans `incidents-connus.md`.
