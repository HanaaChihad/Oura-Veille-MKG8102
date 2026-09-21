# Journal de collecte

Équipe 3, MKG8102, automne 2026. Tenu par la Connaissance et la diffusion jusqu'au 11 septembre ; chaque entrée suivante indique qui l'a rédigée. Le détail de chaque passage sur une source, réussi ou non, est dans la table Journal de collecte d'Airtable (identifiants JC-AAAAMMJJ-CODE). Ce fichier en donne le récit ; la base fait foi pour les chiffres.

## Samedi 5 septembre

Le cours a commencé par la théorie : les formes de veille — concurrentielle, commerciale, technologique et sociétale —, le cycle en six étapes, et la manière de formuler une véritable KIQ. Ensuite, l'atelier pour choisir les rôles et le cas.

À ce moment-là, j'ai travaillé avec Claude pour explorer une première piste : Eli Health, une jeune entreprise de Montréal qui vend un test de cortisol à domicile, le Hormometer. Nous avons cherché ensemble ce qui se disait d'elle en ligne. Elle a levé douze millions de dollars américains en série A, et son histoire est intéressante : elle a démarré en misant sur la santé des femmes et la ménopause, mais son lancement public a plutôt misé sur le stress en général, un sujet qui devenait énorme sur les réseaux sociaux à ce moment-là. Nous avons formulé une KIQ centrale autour de cette tension — Eli Health allait-elle pencher vers le stress général ou revenir vers la santé des femmes ? — avec deux KIQ secondaires pour la nourrir.

L'équipe a finalement préféré un autre cas : Oura Health, le fabricant des bagues ŌURA. Le moment tombait bien, Oura venait de rendre public son formulaire S-1 en vue d'une entrée en bourse, deux jours plus tôt à peine. Cela donnait beaucoup plus de matière fraîche à surveiller.

L'après-midi, l'équipe a commencé à tester si nos premières sources étaient collectables avec Firecrawl.

## Du 6 au 8 septembre

Le travail de collecte s'est poursuivi. Nous avons testé onze sources ; neuf ont répondu directement, deux adresses ne fonctionnaient pas et il a fallu les corriger. La liste des acteurs à surveiller s'est précisée : les concurrents directs RingConn, Ultrahuman et Samsung, et les marques femtech plus petites, Femometer, Evie Ring et Belle Ring.

## Mercredi 9 septembre

Nous avons réalisé que la première version du mandat faisait de la veille sur Oura elle-même, en la traitant comme un acteur externe, alors que nous sommes censés être l'équipe interne d'intelligence marketing d'Oura. C'était une véritable erreur de fond, et non un simple problème de formulation : nous n'avons pas à surveiller ce que notre propre entreprise s'apprête à décider. Nous l'avons corrigée. Le dispositif n'observe plus que l'extérieur, jamais Oura directement — sauf pour la manière dont les autres parlent d'Oura dans les comparatifs ou les avis, ce que nous ne contrôlons pas de toute façon.

La KIQ centrale a été arrêtée le soir même, retenue contre deux autres formulations explorées. Elle demande si l'accès sans frais récurrents aux fonctions de santé des femmes va devenir l'argument de vente dominant chez nos concurrents d'ici le 15 novembre, au point de rendre notre abonnement obligatoire handicapant pour la campagne des Fêtes. Les trois hypothèses ont aussi été réécrites pour s'exclure réellement, ce qui n'était pas le cas auparavant.

Plusieurs faits ont été vérifiés dans la journée. Le S-1 déposé par Oura confirme qu'environ 72 % des cinq millions de membres payants sont des femmes, que cette base croît plus vite que celle des hommes depuis l'exercice 2024, et qu'il existe un modèle de langage propriétaire appelé Oura Women's Health Expert. Nous avons aussi confirmé que Samsung a obtenu une équivalence substantielle de la FDA le 20 juillet pour le dépistage du risque d'apnée du sommeil sur le Galaxy Ring, une première pour une bague en vente libre. Du côté des employeurs, Oura for Employers existe bel et bien, et une enquête SHRM indique que 27 % des employeurs offrent maintenant du soutien pour la ménopause, contre 18 % l'an dernier. Une erreur a été évitée au passage : Ultrahuman n'est pas sans abonnement du tout, elle est sans abonnement obligatoire, et la nuance change le sens de l'argument.

## Jeudi 10 septembre

Les rôles sont désormais nominatifs : Lamia Guellif à la direction, Safaa Chihad aux opérations de veille, Philippe Gariépy responsable des insights, Zakaria Jouahi à l'architecture de données, et moi à la connaissance et à la diffusion.

Philippe a livré une grille de fiabilité claire, fondée sur trois critères : la proximité de la source avec l'information, son indépendance et son historique d'exactitude. En l'appliquant aux sources du bloc 4, le registre MDALL de Santé Canada obtient la cote A ; Best Buy Canada et MobiHealthNews obtiennent B ; RingConn, Ultrahuman, les marques femtech, Wareable et Benefits Canada obtiennent C et doivent toujours être recoupées ; les avis clients obtiennent D et ne comptent jamais seuls. Cela a permis de refaire les blocs 5 et 6 avec des seuils d'alerte liés directement à cette cote.

De mon côté, j'ai travaillé sur les blocs 5 et 6 avec Claude — les destinataires, les seuils et le rythme de diffusion — et j'ai commencé à rassembler mes échanges pour la déclaration d'usage de l'intelligence artificielle. Restaient alors trois choses à boucler : la preuve de collecte des Opérations de veille avec notre propre connecteur, le schéma complet de l'Architecture de données, et la relecture croisée par toute l'équipe.

## Vendredi 11 septembre

Zakaria a pris en charge l'architecture de données et a terminé la base Airtable, les cinq tables avec leurs liens. Cela referme le trou que nous traînions depuis quelques jours : personne n'avait encore ce rôle. La pièce 2 est enfin prête. Safaa a rédigé le bloc 6, le rythme de collecte et de diffusion, avec les seuils fixés avec Philippe. Le tableau de synthèse final compte douze sources : dix conservées, Amazon.ca écartée en échec direct, et le registre MDALL relevé manuellement faute de connecteur.

De mon côté, j'ai finalisé la déclaration d'usage de l'intelligence artificielle et mis le dépôt GitHub en ordre — le mandat, ce journal et les deux pièces jointes. Vérification finale par la Direction avant dépôt, en fin de journée. Deux collectes Firecrawl ont été relancées pour confirmer que la chaîne tient : ultrahuman.com et femometer.com répondent toutes deux. Le titre de la page Femometer Ring Gen2 porte la mention « No Subscription Fee » et la page Ultrahuman Ring AIR indique qu'il n'y a pas de frais d'abonnement récurrents pour accéder à ses données — premier relevé de l'indicateur 1, consigné au journal. Le bloc 4 a été repris pour que chaque source porte son type, sa justification, sa cote détaillée, son connecteur, sa fréquence et son biais ; toute dépendance à un connecteur non branché a été retirée du mandat, et le statut réel de Firecrawl — recherche seulement — y est nommé.

## Jeudi 17 septembre

*Entrée rédigée par la Direction.*

Philippe Gariépy a quitté le cours après la remise du 11 septembre. La Direction reprend le rôle de Responsable des insights et applique la grille de fiabilité aux quinze sources de la base : P, I et H sont inscrits source par source, et chaque biais est écrit dans le champ Biais connu.

Première collecte hebdomadaire réelle, lancée par la Direction avec Firecrawl : treize passages consignés au journal Airtable, neuf fiches créées au statut À valider. Quatre passages n'ont pas produit de fiche, et ils sont consignés comme les autres :

- Whoop et Trustpilot : limite de débit du connecteur (HTTP 429) après dix requêtes dans la même session.
- Evie Ring : aucun résultat pour le domaine eviering.com, sans message d'erreur.
- Peri, communiqué de lancement : aucun communiqué distinct sur le domaine de la marque ; la source fait doublon avec la page produit.

Éléments écartés rendus visibles : pages américaines quand l'indicateur vise le Canada, doublons de tailles d'une même bague, reprises de presse au profit de la page de la marque. Le prix affiché n'apparaît pas dans l'extrait du mode recherche : relevé manuel requis pour l'indicateur 3.

## Samedi 19 septembre — jour de la démonstration

*Entrée rédigée par la Direction.*

Reprise des deux collectes en échec. Whoop, relancée seule : aucune limite rencontrée, ce qui confirme le repli inscrit au registre des incidents. L'abonnement obligatoire y est confirmé : Whoop sert de contre-exemple et appuie H1. Evie Ring : dix résultats, tous tiers, aucun du domaine de la marque ; aucune fiche, la source reste À vérifier. L'absence de preuve n'est pas une preuve d'absence.

Six révisions datées et justifiées dans le champ Motif de révision de la KIQ-1 :

1. Seuil du « handicap » écrit dans les Indicateurs discriminants, avec sa règle de réfutation, son niveau de confiance et l'hypothèse alternative H3 à tenir ouverte.
2. Rôles révisés après le départ de Philippe Gariépy. La Direction cumule les Insights. Compensation : le contrôle 1 (validation des fiches) est délégué aux Opérations de veille ; le contrôle 2 (avant diffusion) reste à la Direction.
3. Source « Peri (IdentifyHer) - communiqué de lancement » écartée pour adresse morte. Retirée du périmètre, pas supprimée.
4. Défaut trouvé dans le champ calculé « Cote proposée » : une note de 0 est confondue avec une case vide. Correction confiée à l'Architecture de données.
5. Première séance de validation, 14 h 30 : sept fiches sur neuf validées. Deux laissées à valider délibérément (Peri et Benefits Canada), crédibilité 3 et source unique sur leur canal : elles attendent un recoupement. La saisie des champs Statut et Validé par a été faite par le connecteur Airtable sur instruction de la Direction, déclarée au niveau AIAS 4.
6. Modèles de revenu inscrits dans la table Acteurs à partir des seules fiches validées : RingConn, Femometer et Ultrahuman en achat unique sans abonnement, Samsung en non indiqué.

Les KIQ secondaires S1, S2 et S3 sont révisées le même jour : indicateurs, décideur et horizon rendus explicites, sans changement de sens.

Lecture du seuil ce jour-là : la Direction a conclu au premier relevé sur trois, les deux conditions réunies, niveau de confiance moyen. Voir la relecture du 21 septembre.

## Lundi 21 septembre — jour du dépôt

*Entrée rédigée par la Direction.*

**Relecture stricte du premier relevé (révision 7 de la KIQ-1).** La condition (a) du seuil exige l'argument « sans abonnement » dans le titre ou la métadescription chez au moins deux des trois concurrents directs présents au Canada. Au 17 septembre, seul RingConn le porte dans son titre. Ultrahuman l'affirme dans le corps de sa page d'achat, pas dans le titre, et sa disponibilité au Canada reste à vérifier dans la table Acteurs. Samsung Canada ne le porte pas. La condition (a) n'est donc pas établie au sens strict ; la condition (b) l'est (Best Buy Canada, cote B). Le relevé du 17 septembre ne compte pas comme premier relevé sur trois. Le jugement du 19 septembre allait plus loin que la règle écrite le même jour : c'est la règle qui fait foi.

**Rétroaction du professeur appliquée dans la base.**

- Charge hiérarchisée (révision 8) : les groupes S1, S2 et S3 du bloc 4 passent en premier rang ; la presse spécialisée, les avis clients et les avantages sociaux en second rang, à fréquence réduite, sans retrait du mandat.
- Firecrawl vérifié une quatrième fois (révision 9), sur Best Buy Canada et sur le registre MDALL : aucun outil d'extraction, le relevé des prix reste manuel. Le test rapporte un fait nouveau : Best Buy Canada consacre une catégorie aux bagues « sans abonnement ». Fiche créée, à valider.
- Premier relevé du registre MDALL (JC-20260921-MDALL), par son formulaire de recherche. Aucune licence canadienne pour RingConn, Ultrahuman, Movano, IdentifyHer ni pour un appareil « Galaxy Ring ». Samsung Electronics détient quatre licences de fonctions logicielles, dont une fonction d'apnée du sommeil délivrée en 2024, sans bague nommée ni fonction de santé des femmes. La marque Femometer a huit appareils homologués en santé reproductive, pas sa bague. Trois fiches créées, à valider, dont une fiche « rien trouvé ». S2 reste à « pas encore », désormais vérifié à la source cotée A.
- Règle « rien trouvé » (révision 10), donnée en rencontre le 17 septembre, appliquée pour la première fois.
- Quatre dates inventées retirées du journal (révision 11) : des lignes de test créées le 11 septembre portaient la date du 15.

**À trancher à la prochaine validation.** Samsung figure au registre MDALL, ce qui touche le seuil d'alerte 4, mais pour des fonctions sans lien avec la santé des femmes et depuis 2021 et 2024. La Direction décide si le seuil 4 vise toute inscription ou seulement une inscription nouvelle sur une fonction de santé des femmes, et l'écrit.

**Dépôt remis à niveau** pour l'échéance de 23 h 59 : Skill d'équipe dans le dossier `fiche-de-veille/`, configuration documentée avec les indicateurs du dispositif, registre des incidents complété, grille de fiabilité alignée sur la base, mandat en texte avec le numéro d'équipe, gabarit et exemple de brief séparés, déclarations d'usage de l'IA complétées.

**Correction de l'entrée du 11 septembre.** Amazon.ca n'a pas été « écartée ». C'est le connecteur qui a échoué ; la source reste au mandat (bloc 4), au statut À vérifier, en attente d'un relevé manuel.
