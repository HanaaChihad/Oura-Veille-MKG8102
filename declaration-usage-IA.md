# Déclaration d'usage de l'intelligence artificielle

Équipe 3, MKG8102. Échelle AIAS révisée de Perkins, Roe et Furze (2025). Chaque membre répond de la section qui le concerne ; l'équipe répond solidairement de l'ensemble.

## Niveaux déclarés

| Travail | Niveau AIAS |
|---|---|
| Mandat de veille et architecture du dispositif (équipe, 11 septembre) | 3 — AI Collaboration |
| Plateforme de veille automatisée, démonstration et dépôt (équipe, 19 et 21 septembre) | 4 — Full AI |
| Prototype de veille individuel (2 octobre) | 4 — Full AI |
| Réflexion analytique individuelle (2 octobre) | 3 — AI Collaboration : l'analyse et le jugement final restent humains |

## Outils et modèles

Claude (Anthropic), en conversation et en mode Cowork, avec les connecteurs Firecrawl, Airtable, Gmail et GitHub, et le navigateur intégré de Claude (formulaire du registre MDALL, enregistrement de ce dépôt). Perplexity a servi une fois, du 5 au 11 septembre, à produire une seconde version de l'échelle de fiabilité, écartée après comparaison. Aucun autre outil génératif.

## Ce qui reste humain, sans exception

- Le choix du cas, de la KIQ, des hypothèses et du seuil du mot « handicap ».
- L'attribution de la cote qui fait foi (champ Fiabilité).
- La décision de valider ou de rejeter une fiche (contrôle 1) et d'autoriser une diffusion (contrôle 2).
- Aucune date, aucune adresse, aucune citation n'a été générée : chacune vient d'une page réellement collectée ou reste vide.

## 1. Du 5 au 11 septembre — mandat (AIAS 3)

Repris de l'annexe A du mandat remis le 11 septembre.

| Membre et rôle | Requêtes | Généré par l'IA | Vérifié, modifié ou rejeté |
|---|---|---|---|
| Lamia Guellif — Direction de l'intelligence marketing | Collecte sur les produits et offres des concurrents ; génération et confrontation de candidates de KIQ ; tests de collectabilité des sources ; vérification de faits sur sources primaires | Collecte documentaire du 7 septembre ; trois candidates de KIQ et leur évaluation sur les cinq propriétés ; mise en forme du mandat | Formulation « déplacement de la demande canadienne » rejetée comme non falsifiable en sources ouvertes. Candidate portant sur le détail physique écartée faute de sources ouvertes. Périmètre retourné vers l'environnement. Homologation FDA de Samsung vérifiée dans la base de la FDA. Chiffre de composition de la base d'utilisateurs corrigé au profit du S-1. « Sans abonnement » corrigé en « sans abonnement obligatoire » pour Ultrahuman |
| Safaa Chihad — Opérations de veille | Portefeuille de sources ouvertes ; tests réels de collectabilité sur douze sources, répétés un second jour ; vérification directe des connecteurs | Tableau de synthèse des douze sources ; journal de collecte ; chaîne d'ingestion proposée ; guide de captures d'écran | Chiffre de coût total sur deux ans (Wareable) écarté faute de reconfirmation. URL Samsung corrigée après une erreur 404. Amazon.ca et MDALL reclassés : le connecteur est remplacé, pas la source. Statut des connecteurs vérifié trois fois sur deux jours. Aucune cote générée par l'IA |
| Zakaria Jouahi — Architecture de données | Champs et liens des cinq tables ; création de la base par le connecteur ; tableau du bloc 4 et schéma de la pièce 2 | Structure des cinq tables, formule de la cote proposée, saisie des sources et des lignes de journal à partir des documents d'équipe | Aucune cote, date ni adresse générée : ces champs restaient vides tant que les Insights et les Opérations ne les avaient pas fournis. Modélisation en sept tables écartée. Chaque table validée avant création |
| Philippe Gariépy — Responsable des insights | Échelle de fiabilité applicable au bloc 4 ; comparaison de deux propositions | Deux versions de l'échelle (Perplexity, Claude) ; formulation des trois critères et du barème | Version Perplexity écartée. Notation P, I, H et cotes A à F faites à la main, sans assistance. Analyse des biais rédigée de la même façon |
| Hanaa Chihad — Connaissance et diffusion | Rédaction des livrables, destinataires et seuils du bloc 5 ; tenue du journal | Première rédaction du bloc 5 ; mise en forme minimale du journal | Seuils réécrits pour qu'aucun ne se déclenche sans cote minimale. Exemple de bout en bout construit à la main. Journal tenu au jour le jour, erreur du 9 septembre conservée |

## 2. Du 12 au 21 septembre — plateforme, démonstration et dépôt (AIAS 4)

### Lamia Guellif — Direction de l'intelligence marketing, cumulant les Insights depuis le 19 septembre

- **Collecte.** Collectes du 17 et du 19 septembre lancées dans Claude (Cowork) avec les connecteurs Firecrawl et Airtable. Claude a produit les neuf fiches et les lignes de journal à partir des résultats de recherche ; aucune date, adresse ou citation n'a été ajoutée hors de ce que rendait la page.
- **Cotation.** Notes P, I et H des quinze sources arrêtées par la Direction le 17 septembre, avec l'appui de Claude. La cote qui fait foi, dans le champ Fiabilité, est celle de la Direction.
- **Validation.** Le jugement de validation des sept fiches du 19 septembre appartient à la Direction, après vérification de l'adresse, de l'extrait, du rattachement à la KIQ et de la cote. La saisie des champs Statut et Validé par a été faite par le connecteur Airtable, sur instruction de la Direction, au cours de la même séance. C'est déclaré dans la base (KIQ-1, révision 5) et l'historique de révision d'Airtable en porte la trace.
- **Révisions de la KIQ.** Les révisions datées de la KIQ-1 et des KIQ secondaires ont été rédigées avec Claude à partir des décisions de la Direction. Les modèles de revenu de la table Acteurs ont été inscrits par le connecteur à partir des seules fiches validées.
- **Préparation de la démonstration.** Déroulé, fiches d'orateurs et texte de présentation rédigés avec Claude, puis relus et modifiés.
- **Dépôt et base, 21 septembre.** Les fichiers de ce dépôt ont été rédigés par Claude à partir de la base Airtable, du mandat et du journal, puis relus par la Direction avant l'enregistrement. La relecture stricte du seuil du « handicap » (révision 7) a été signalée par Claude et arrêtée par la Direction. Sur instruction de la Direction, Claude a appliqué dans la base la rétroaction du professeur (rang des sources, fréquences, révisions 7 à 11), fait le test Firecrawl et le premier relevé du registre MDALL, et créé les quatre fiches qui en sortent, toutes au statut À valider : aucune n'a été validée par le modèle.
- **Refusé ou corrigé.** Aucune fiche validée en bloc : deux fiches laissées à valider faute de recoupement. Le défaut du champ calculé « Cote proposée » a été documenté plutôt que masqué.

### Safaa Chihad — Opérations de veille

Usage de l'IA minimal sur cette période : l'essentiel du travail a été fait à la main. Les usages sont de même nature que ceux qu'elle a déclarés du 5 au 11 septembre (section 1), et les mêmes règles s'appliquent : aucune cote, aucune date, aucune adresse générée par l'IA. Déclaration transmise à la Direction le 21 septembre.

### Zakaria Jouahi — Architecture de données

Usage de l'IA minimal sur cette période : l'essentiel du travail a été fait à la main. Les usages sont de même nature que ceux qu'il a déclarés du 5 au 11 septembre (section 1), et les mêmes règles s'appliquent : aucune cote, aucune date, aucune adresse générée par l'IA. Déclaration transmise à la Direction le 21 septembre.

### Hanaa Chihad — Connaissance et diffusion

- Aide à la rédaction et à la reformulation des blocs 4, 5 et 6 du mandat, à partir des décisions déjà prises par l'équipe.
- Aide à la rédaction du journal de collecte, à partir des faits et des dates fournis par l'équipe.
- Structuration de ce dépôt GitHub et rédaction du gabarit de brief.
- L'IA n'a pas choisi le cas, la KIQ, les hypothèses ni le seuil du mot « handicap ». Elle n'a validé aucune fiche ni autorisé aucune diffusion. Elle n'a inventé aucun fait ni aucune source.

## Traçabilité

Chaque échange avec l'IA utilisé pour produire ce dépôt est conservé et peut être montré sur demande. Dans la base, la colonne Opératrice ou opérateur du journal, le champ Validé par des fiches et le champ Motif de révision des KIQ disent qui a fait quoi, et quand.
