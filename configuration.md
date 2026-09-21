# Configuration du dispositif

Équipe 3, MKG8102. Ce fichier permet à une personne qui n'a jamais vu le dispositif de relancer une collecte avec le seul dépôt. État au 21 septembre 2026.

## 1. Ce qu'il faut avant de commencer

- Un compte Claude avec les connecteurs **Airtable** et **Firecrawl** activés. **Gmail** sert à la diffusion.
- Un accès éditeur à la base Airtable « Veille MKG8102 — Oura », à demander à l'Architecture de données. Sans accès éditeur, le lien en lecture seule permet de dupliquer la base : https://airtable.com/appoRS4zO7UKMsMeH/shrXmbGYgDj1zyyqN
- La Skill de l'équipe, téléversée dans Claude (voir l'étape 1 de la section 5).

Aucune clé, aucun jeton et aucun mot de passe ne figurent dans ce dépôt, ni dans une conversation, un projet ou la base. Les connecteurs s'autorisent dans la page Connecteurs de Claude.

## 2. Connecteurs

| Connecteur | Rôle dans le dispositif | Limite connue | Repli |
|---|---|---|---|
| Firecrawl | Repérage et collecte des pages des sources | Mode recherche seulement : titre, adresse, description. Aucun outil d'extraction de page, donc pas de prix affiché sauf s'il figure dans la description. Vérifié quatre fois, la dernière le 21 septembre sur Best Buy Canada et sur le registre MDALL. Limite de débit HTTP 429 après une dizaine de requêtes dans la même session | Une source à la fois ; prix relevés à la main |
| Airtable | Mémoire du dispositif : les cinq tables | Crée et met à jour des enregistrements ; ne crée pas de champ et ne modifie ni une formule ni la description d'un champ | Ces modifications se font dans l'interface d'Airtable |
| Gmail | Canal de diffusion 1 : brief hebdomadaire et alertes à la vice-présidence Marketing | — | — |
| Relevé manuel | Registre MDALL de Santé Canada, Amazon.ca, prix affichés | Dépend d'une personne ; à consigner au journal avec le connecteur « Manuel » | — |
| Apify | Non branché. Aucune source de la table Sources n'en dépend | — | — |
| GitHub | Ce dépôt, privé | — | — |

Le journal garde trois tests du 11 septembre étiquetés « Apify » (Best Buy Canada, Amazon.ca, Trustpilot) : l'étiquette désigne le connecteur visé à ce moment-là. Aucune collecte depuis le 17 septembre ne passe par Apify.

## 3. La base Airtable « Veille MKG8102 — Oura »

Cinq tables liées. Chaque fiche est reliée à sa source, à son acteur, à sa KIQ et à la ligne de journal qui l'a produite : « d'où vient ce fait » se répond en un clic.

| Table | Une ligne = | Champs qui comptent | Liée à |
|---|---|---|---|
| KIQ | Une question : KIQ-1 et les secondaires S1, S2, S3 | Énoncé, Hypothèses rivales, Indicateurs discriminants (dont le seuil du handicap), Angle mort assumé, Date et Motif de révision | Sources, Fiches, KIQ secondaires |
| Acteurs | Une entreprise surveillée (neuf ; Oura exclue par conception) | Type, Disponible au Canada, Modèle de revenu (mis à jour seulement depuis une fiche validée), Statut de surveillance | Sources, Fiches |
| Sources | Une page ou un site surveillé (quinze) | Adresse, Type, P, I, H, Fiabilité, Biais connu, Connecteur, Fréquence, Jour de relevé, Dernière collecte, État, Motif d'écartement | Acteurs, KIQ, Fiches, Journal |
| Fiches de veille | Un fait | Les champs de la Skill, plus Collecte d'origine et Connecteur d'origine | Source, Acteur, KIQ, Journal |
| Journal de collecte | Un passage sur une source, réussi ou non | Identifiant JC-AAAAMMJJ-CODE, Date et heure, Connecteur, Résultat, Éléments retenus et écartés, Type d'erreur, Erreurs, Opératrice ou opérateur | Source, Fiches produites |

Champs de traçabilité (remplis par la machine) : Date de captation, Adresse exacte, Extrait cité, Source, Connecteur d'origine. Champs de contrôle (remplis par un humain seulement) : Statut, Validé par, Motif de rejet, Fiabilité.

Vues de la table Fiches de veille :

| Vue | Usage |
|---|---|
| Fiches à valider | File d'attente du contrôle 1 |
| Validation | Vue en colonnes (kanban), pour la séance de validation |
| Fiches validées | Canal de diffusion 2 : ce que la décideuse peut consulter en lecture seule |
| Grid view | Vue de travail complète |

## 4. Les sources, leur rang et leur rythme

La table Sources fait foi. Relevé au 21 septembre 2026.

Révision du 21 septembre, à la demande du professeur : les groupes S1, S2 et S3 du bloc 4 du mandat (pages des concurrents, détail canadien, registre MDALL) suffisent à départager H1, H2 et H3. Ils passent en **premier rang**. La presse spécialisée (S4), les avis clients et les avantages sociaux (S5) sont de la couverture : **second rang**, fréquence réduite, jamais retirés du mandat. Le rang est écrit en tête du champ Justification de chaque source.

| Source | Groupe | Rang | Cote | Connecteur | Fréquence | Jour | Dernière collecte | État |
|---|---|---|---|---|---|---|---|---|
| RingConn Gen 3 - page produit | S1 | Premier | C | Firecrawl | Hebdomadaire | Mardi | 17 sept. | Active |
| Ultrahuman Ring AIR - page de prix | S1 | Premier | C | Firecrawl | Hebdomadaire | Mardi | 17 sept. | Active |
| Samsung Galaxy Ring Canada - page produit | S1 | Premier | C | Firecrawl | Hebdomadaire | Mardi | 17 sept. | Active |
| Femometer Ring Gen2 - page produit | S1 | Premier | C | Firecrawl | Bimensuelle | Mardi | 17 sept. | Active |
| Evie Ring - page produit | S1 | Premier | C | Firecrawl | Hebdomadaire | Lundi | 19 sept. | À vérifier |
| Peri (IdentifyHer) - page produit | S1 | Premier | C | Firecrawl | Hebdomadaire | Lundi | 17 sept. | Active |
| Whoop - page produit | S1 | Premier | C | Firecrawl | Bimensuelle | Lundi | 19 sept. | Active |
| Best Buy Canada - bagues connectées | S2 | Premier | B | Firecrawl, prix à la main | Hebdomadaire | Mardi | 21 sept. | Active |
| Amazon.ca - bagues connectées | S2 | Premier | B | Manuel | Hebdomadaire | Mardi | — | À vérifier |
| Santé Canada - registre MDALL | S3 | Premier | A | Manuel | Mensuelle, et à chaque annonce d'un concurrent | — | 21 sept. | Active |
| Wareable - comparatif des bagues connectées 2026 | S4 | Second | C | Firecrawl | Bimensuelle (hebdomadaire avant le 21 sept.) | Mardi | 17 sept. | Active |
| MobiHealthNews - homologation FDA Samsung | S4 | Second | B | Firecrawl | Mensuelle (bimensuelle avant le 21 sept.) | — | 17 sept. | Active |
| Trustpilot - RingConn | S5 | Second | D | Firecrawl | Mensuelle (bimensuelle avant le 21 sept.) | — | — | À vérifier |
| Benefits Canada - ménopause en milieu de travail | S5 | Second | C | Firecrawl | Mensuelle | — | 17 sept. | Active |
| Peri (IdentifyHer) - communiqué de lancement | S1 | — | — | — | — | — | — | Écartée (adresse morte) |

Même jour de la semaine à chaque passage : sinon les prix relevés fabriquent une fausse tendance. Relevé quotidien prévu du 23 au 30 novembre 2026 (mandat, bloc 6).

## 5. Relancer une collecte, pas à pas

1. **Installer la Skill.** Compresser le dossier `fiche-de-veille/` de ce dépôt en fichier .zip, puis dans Claude : Personnaliser › Skills › + › téléverser. La Skill « fiche-de-veille » apparaît dans la liste.
2. **Ouvrir une conversation neuve** et y activer Firecrawl et Airtable.
3. **Vérifier l'accès** en tapant : « Liste les tables de la base Veille MKG8102 — Oura ». Les cinq tables doivent apparaître.
4. **Choisir la source** dans la table Sources : état « Active », jour de relevé égal au jour de la collecte. Noter son adresse et la KIQ qu'elle sert.
5. **Lancer la collecte** avec la phrase de l'atelier du 5 septembre, en remplaçant ce qui est entre crochets :

   > Va chercher cette page avec Firecrawl : [adresse de la source]. Fais-en une fiche de veille pour la KIQ [code et énoncé de la KIQ] et crée l'enregistrement dans la table Fiches de veille de la base Veille MKG8102 — Oura, statut à valider. Ajoute une ligne dans Journal de collecte avec la date, le connecteur, le nombre d'éléments retenus et les erreurs rencontrées. N'invente aucune donnée absente de la page : laisse le champ vide et signale-le.

6. **Une source à la fois.** Enchaîner toute la liste déclenche la limite de débit (HTTP 429).
7. **Si Firecrawl ne rend rien**, ouvrir la page dans un navigateur, tout sélectionner, copier, puis :

   > Voici le texte d'une page que Firecrawl n'a pas pu lire. Son adresse est [adresse]. Fais-en une fiche de veille pour la KIQ [énoncé] et crée l'enregistrement dans la table Fiches de veille, statut à valider. [texte collé]

   Inscrire le connecteur « Manuel » au journal.
8. **Vérifier la ligne au journal.** Pas de ligne au journal, pas de collecte. Un échec s'inscrit comme un succès, avec son type d'erreur.
9. **Mettre à jour la source** : champ Dernière collecte.

## 6. Contrôles humains

| Contrôle | Quand | Qui | Ce qui est vérifié |
|---|---|---|---|
| 1 — Validation | Avant qu'une fiche existe pour la décideuse | Opérations de veille, par délégation depuis le 19 septembre | Adresse collectée, extrait cité mot pour mot, rattachement à la KIQ, cohérence avec la cote de la source. Puis Statut « Validé » et Validé par, ou Statut « Rejeté » et l'un des trois motifs : date inventée, citation inexacte, hors KIQ |
| 2 — Diffusion | Avant tout envoi à la décideuse | Direction de l'intelligence marketing | Chaque affirmation du brief ou de l'alerte remonte à une fiche validée |

Une fiche non validée n'existe pas pour la décideuse : elle n'est ni citée dans un brief, ni déclencheur d'alerte. Le modèle de revenu d'un acteur ne se met à jour qu'à partir d'une fiche validée.

Écart assumé. Le départ du Responsable des insights a fait tomber les deux contrôles sur la Direction ; la révision 2 de la KIQ-1 délègue donc le contrôle 1 aux Opérations de veille. La première séance de validation, le 19 septembre, a pourtant été tenue par la Direction (révision 5 : sept fiches validées, deux laissées à valider faute de recoupement). La délégation reste à exercer dans la base.

## 7. Diffusion

| Livrable | Canal | Rythme | Condition |
|---|---|---|---|
| Brief BLUF d'une page | Gmail, à la vice-présidence Marketing, Amérique du Nord | Le vendredi avant midi | Contrôle 2 passé |
| Alerte de cinq lignes : fait, seuil franchi, ampleur, délai, options | Gmail | Le jour même | Seuil franchi et confirmé par une source A ou B, ou par deux sources indépendantes si la cote est C |
| Fiches validées | Vue « Fiches validées », lecture seule | En continu | Statut « Validé » |

Gabarit du brief : `gabarit-brief.md`. Exemple rempli : `exemple-brief-VP-marketing.md`.

## 8. Seuils

Seuils d'alerte (mandat, bloc 6) :

1. Un concurrent monte « sans abonnement » dans son titre ou sa métadescription. Cote C acceptée si recoupée par une deuxième source indépendante.
2. Une bague femtech apparaît chez un détaillant canadien surveillé. Cote B ; Best Buy Canada suffit seul.
3. Un prix affiché varie d'au moins 10 % d'une collecte à l'autre. Cote B.
4. Un concurrent est inscrit au MDALL ou annonce un statut réglementaire. Cote A si vu au registre, C si vu chez le concurrent, donc à recouper.

Les avis clients ne déclenchent jamais d'alerte.

Seuil du « handicap » (KIQ-1, ajouté le 19 septembre 2026). Le mot « handicap » est un jugement, pas une observation : aucun indicateur ne l'observe directement. Il y a handicap lorsque, sur trois relevés hebdomadaires consécutifs, les deux conditions sont réunies : (a) l'argument « sans abonnement » occupe le titre ou la métadescription chez au moins deux des trois concurrents directs présents au Canada ; et (b) au moins une bague sans abonnement obligatoire est référencée chez un détaillant canadien surveillé, source cotée B au minimum. Réfutation : si l'une des deux conditions tombe pendant deux relevés consécutifs, ou si le coût total sur deux ans cesse de figurer comme critère de classement dans les comparatifs suivis, on conclut à l'absence de handicap et H1 reprend l'avantage.

## 9. Règles de collecte

**Ce qui est permis.** Les quatre règles du cours s'appliquent à chaque source : contenus accessibles sans authentification ; conditions d'utilisation respectées ; aucune donnée personnelle conservée (les avis clients sont lus en agrégat, jamais un par un) ; n'automatiser que ce que le mandat justifie.

**Amazon.ca, ou comment on contourne une décision d'affaires.** Amazon.ca bloque la collecte automatisée : c'est une décision du site, et nous ne la contournons pas par un outil. Le relevé est fait à la main, par une personne, sur la page publique, comme le ferait une acheteuse, et il se limite à ce que l'indicateur 3 exige : le prix affiché, une fois par semaine. Le blocage est inscrit au journal et au registre des incidents, pas masqué.

**« Rien trouvé » s'écrit.** Quand une source répond mais ne publie rien de nouveau, le passage est inscrit au journal avec zéro élément retenu et la mention « rien trouvé ». Une collecte qui ne laisse aucune trace quand elle ne trouve rien rend la régularité incalculable.

**Les sources lentes.** Le registre MDALL de Santé Canada publie avec retard. On ne l'attend pas : on l'interroge une fois par mois et à chaque annonce d'un concurrent, par son formulaire de recherche (nom d'entreprise, puis nom d'appareil). Condition de déclenchement : un acteur surveillé apparaît avec un appareil de santé des femmes, ce qui franchit le seuil d'alerte 4 avec une source cotée A. Quand rien n'apparaît, une fiche « rien trouvé » datée est créée et rattachée à S2, en plus de la ligne au journal.

## 10. Mesurer le dispositif lui-même

Les six indicateurs de la KIQ mesurent le monde. Ceux-ci mesurent la veille. Calculés sur la table Journal de collecte, hors tests de collectabilité du 6 au 11 septembre, au 21 septembre 2026.

| Indicateur | Valeur | Lecture |
|---|---|---|
| Passages consignés | 17 (13 le 17 sept., 2 le 19, 2 le 21) | Chaque passage a sa ligne, échecs compris |
| Taux de succès | 12 sur 17 (71 %) ; 2 partiels ; 3 erreurs (18 %) | Les trois erreurs : deux limites de débit (HTTP 429) et un domaine muet |
| Couverture des sources | 11 sources sur 14 ont au moins un passage réussi (79 %) ; en premier rang, 8 sur 10 | Manquent Evie Ring et Amazon.ca en premier rang, Trustpilot en second |
| Sélectivité | 14 éléments retenus sur 77 vus | Ce qui est écarté est compté, pas oublié |
| Fiches produites | 13 : 7 validées, 0 rejetée, 6 à valider | Un élément retenu le 19 sept. (Whoop) n'a pas encore sa fiche |
| Latence entre le fait et sa captation | Mesurable sur 3 fiches sur 13 : 14 jours (Wareable), 59 jours (Samsung, décision FDA), 725 jours (licence canadienne de Samsung, délivrée en 2024) | La plupart des pages ne datent pas le fait. Et le dispositif découvre tard des faits anciens : la licence canadienne de Samsung existait depuis deux ans |
| Régularité | 1 relevé hebdomadaire complet, le 17 sept., un jeudi | Le jour fixé est le mardi ; prochain relevé prévu le 22 septembre |

## 11. Ce que le dispositif ne fait pas encore

- Les collectes consignées au journal au 21 septembre ont toutes été lancées à la main, source par source (colonne Opératrice ou opérateur du journal).
- Aucun relevé manuel d'Amazon.ca n'est encore consigné au journal.
- Veille sociétale exclue par le mandat : le dispositif ne verra ni un retournement d'opinion sur la collecte de données de santé intime, ni une controverse sur la fiabilité de signaux non homologués en périménopause (angle mort assumé, table KIQ).
