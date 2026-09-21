# Incidents connus et solutions de repli

Équipe 3, MKG8102. Ce fichier consigne les pannes et les défauts rencontrés depuis le 5 septembre 2026, et le repli retenu pour chacun. Chaque incident a sa trace dans la base Airtable (table Journal de collecte, ou champ Motif de révision de la KIQ-1). Il est mis à jour à chaque collecte.

## 1. Connecteurs et sources

| Quand | Ce qui s'est passé | Repli retenu | Trace |
|---|---|---|---|
| 6 au 8 sept. | Deux adresses sur onze ne répondaient pas au connecteur. | Adresse exacte de remplacement retrouvée sur le site de l'acteur. | Journal du dépôt, 6 au 8 sept. |
| 6 au 11 sept. | Adresse de la page Galaxy Ring de Samsung en erreur 404 au premier essai. | Adresse corrigée, puis collecte réussie. | Mandat, annexe A (Opérations de veille) |
| 6 au 11 sept., puis 21 sept. | Firecrawl ne fonctionne qu'en mode recherche : titre, adresse et description, sans extraction de la page. Vérifié directement trois fois sur deux jours distincts, puis une quatrième fois le 21 septembre à la demande du professeur, sur une page de prix qui fonctionne déjà (Best Buy Canada) et sur le registre MDALL : le connecteur n'expose aucun outil d'extraction. | Le mode recherche suffit pour l'indicateur 1 (position de « sans abonnement » dans le titre et la métadescription). Les prix affichés sont relevés à la main et consignés au journal. | Mandat, bloc 4 et pièce 1 ; JC-20260921-BESTBUY |
| 11 sept. | Amazon.ca : échec direct, page bloquée au connecteur. | Relevé manuel. La source reste : elle est imposée par le mandat. C'est le connecteur qu'on remplace, pas la source. Aucun relevé manuel n'est encore consigné au journal. | JC-TEST-07 ; Sources, état À vérifier |
| 11 sept. | Registre MDALL de Santé Canada : le registre est un formulaire de recherche, que le mode recherche de Firecrawl ne remplit pas. Le registre publie aussi avec retard. | Consultation du formulaire depuis le navigateur, mensuelle et à chaque annonce d'un concurrent. Le retard est accepté : une absence au registre n'exclut pas une homologation récente. Premier relevé consigné le 21 septembre : trois fiches, dont une fiche « rien trouvé ». | JC-TEST-08 ; JC-20260921-MDALL |
| 21 sept. | Le formulaire du registre MDALL répond lentement, une quarantaine de secondes par requête ; plusieurs requêtes lancées ensemble dépassent le délai de l'outil. | Une requête à la fois, résultats notés au fur et à mesure. | JC-20260921-MDALL |
| 17 sept. | Limite de débit du connecteur (HTTP 429) après dix requêtes dans la même session : Whoop et Trustpilot non collectées. | Étaler les passages, une source à la fois, plutôt que lancer toute la liste d'un coup. Repli vérifié le 19 sept. : Whoop relancée seule, sans limite rencontrée. Trustpilot reste à reprendre. | JC-20260917-WHOOP, JC-20260917-TRUSTPILOT, JC-20260919-WHOOP |
| 17 sept. | Evie Ring : aucun résultat pour le domaine eviering.com, sans message d'erreur. | Reprise le 19 sept. : dix résultats, tous tiers, aucun du domaine de la marque. Aucune fiche : le fait ne peut pas être établi par la source primaire visée. Source au statut À vérifier. | JC-20260917-EVIERING, JC-20260919-EVIERING |
| 17 sept. | Peri : aucun communiqué de lancement distinct sur le domaine de la marque, seulement des reprises de presse tierce. La source faisait doublon avec la page produit. | Source « communiqué de lancement » écartée pour adresse morte le 19 sept. ; la page produit reste active. Retirée du périmètre, pas supprimée : la décision est réversible. | JC-20260917-PERI-COMMUNIQUE ; KIQ-1, révision 3 |
| 17 et 19 sept. | Le prix affiché n'apparaît pas dans l'extrait rendu par le mode recherche (Best Buy Canada, Whoop). | Relevé manuel requis pour l'indicateur 3. Aucune fiche ne déduit un prix. | JC-20260917-BESTBUY, JC-20260919-WHOOP |

## 2. Défauts trouvés dans la base elle-même

| Quand | Ce qui s'est passé | Repli retenu | Trace |
|---|---|---|---|
| 19 sept. | Le champ calculé « Cote proposée » de la table Sources teste les cellules vides avec `BLANK()`, qui confond une note de 0 avec une absence de note. Aucune cote n'est proposée pour les sources qui ont un 0 sur un critère, c'est-à-dire les moins fiables (constaté sur Trustpilot : P 0 + I 1 + H 1 = 2, cote D). | La cote humaine du champ Fiabilité fait foi ; le défaut n'a jamais faussé une cote. Correction confiée à l'Architecture de données : remplacer chaque test `{champ} = BLANK()` par `{champ} & "" = ""`. Non appliquée au 21 septembre. | KIQ-1, révision 4 |
| À partir du 19 sept. | Le connecteur Airtable crée et met à jour des enregistrements, mais refuse de modifier une formule ou la description d'un champ, et de créer un champ (constaté le 21 septembre en voulant ajouter un champ Rang à la table Sources). | Ces modifications se font dans l'interface d'Airtable par une personne éditrice de la base. Le rang des sources est écrit en tête du champ Justification en attendant. | KIQ-1, révision 8 |
| 21 sept. | Quatre lignes de test du journal (JC-TEST-09 à 12), créées le 11 septembre, portaient la date du 15 septembre, alors que leur note dit la date non indiquée. Une date inventée est le motif de rejet le plus grave. | Champ vidé : une date qu'on ne peut pas établir reste vide. | KIQ-1, révision 11 |

## 3. Erreurs de méthode

| Quand | Ce qui s'est passé | Repli retenu | Trace |
|---|---|---|---|
| 9 sept. | La première version du mandat faisait de la veille sur Oura elle-même, alors que l'équipe est la fonction d'intelligence marketing interne d'Oura. | Mandat corrigé : le dispositif n'observe que l'extérieur. La règle est inscrite dans la Skill (règle 1 des règles nées de nos erreurs). | Journal du dépôt, 9 sept. |
| 9 sept. | Ultrahuman décrite comme « sans abonnement », alors qu'elle est « sans abonnement obligatoire ». | Corrigé après vérification de la page d'achat. Règle 2 de la Skill. | Mandat, annexe A |
| 11 sept. | Chiffre de coût total sur deux ans (Wareable) non reconfirmé au second test. | Écarté tant qu'il n'est pas vérifié sur la page. Règle 7 de la Skill. | Mandat, annexe A |

## 4. Si un appel d'outil échoue en direct

Le dire à voix haute, montrer ce fichier comme preuve que l'équipe a déjà un plan de repli, et continuer avec une source de secours déjà testée plutôt que d'improviser. Consigner l'échec au journal comme un succès : une source qui ne répond pas ne disparaît pas, elle s'inscrit au journal.
