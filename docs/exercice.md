# Etude de cas 1:

Votre oncle, restaurateur, vous demande de lui réaliser un logiciel de gestion des commandes de repas. Voici les indications qu’il vous donne :

Il souhaite pouvoir gérer certaines informations concernant ses employés : nom, prénom, adresse complète, téléphone et diplôme.

Au niveau de la prise de commande, il souhaite savoir si elle porte sur le service de midi ou celui du soir et à quelle date elle a été passé.

Pour certains calculs statistiques, il souhaite aussi savoir quelle table a passé la commande et quel serveur l’a prise.

La carte du restaurant propose l’ensemble des plats d’entrées, principaux et desserts. Les menus proposés sont un assemblage des plats à la carte. La carte des vins propose une sélection de vins qui sont stockés dans la cave du restaurant. Votre oncle désire connaître pour chaque bouteille son millésime, sa date d’achat, son prix d’achat et son prix de vente. Il voudrait aussi saisir pour chaque cru les informations concernant le viticulteur (nom, prénom, adresse complète, téléphone). A l’heure actuelle, votre oncle, amoureux du vin, met sur chaque goulot de chaque bouteille une étiquette contenant le prix d’achat ainsi que la date d’achat. Votre système doit pouvoir remplacer ce traitement manuel.

Ensuite, certaines boissons comme les apéritifs, les digestifs, les sodas ou les cafés sont gérés de façon simpliste juste par leur libellé et leur prix de vente. Chaque serveur prenant une commande saisit l’ensemble des informations sur un PocketPC qui transmet la commande via Wiki sur un ordinateur central.


**Travail à faire :**

- Établir un dictionnaire de données.
- Identifier les DF.
- Établir le Modèle Conceptuel de Données. 

**Correction**

**1- Dictionnaire des Données**

| Nom                |  Format   | Longueur | T Elementaire | T Calculé | R.Calcul | R.Gestion | Document |
| ------------------ | :-------: | -------: | ------------- | --------- | -------- | --------- | -------- |
| IdentifiantEmploye | AlphaNum  |      255 | X             |           |          |           |          |
| nomEmploye         | AlphaNum  |      255 | X             |           |          |           |          |
| prénomEmploye      | AlphaNum  |      255 | X             |           |          |           |          |
| adresseEmploye     | AlphaNum  |      255 | X             |           |          |           |          |
| téléphoneEmploye   | AlphaNum  |      255 | X             |           |          |           |          |
| diplômeEmploye     | AlphaNum  |      255 | X             |           |          |           |          |
| CompAdresseEmploye | AlphaNum  |      255 | X             |           |          |           |          |
| CodePostalEmploye  | AlphaNum  |      255 | X             |           |          |           |          |
| VilleEmploye       | AlphaNum  |      255 | X             |           |          |           |          |
| IdentifiantBout    | AlphaNum  |      255 | X             |           |          |           |          |
| MillesimeBout      | AlphaNum  |      255 | X             |           |          |           |          |
| DateAchatBout      |   Date    |          | X             |           |          |           |          |
| PrixAchatBout      | Numerique |          | X             |           |          |           |          |
| PrixVenteBout      | Numerique |          | X             |           |          |           |          |
| IdentifiantViti    | AlphaNum  |      255 | X             |           |          |           |          |
| NomViti            | AlphaNum  |      255 | X             |           |          |           |          |
| PrenomViti         | AlphaNum  |      255 | X             |           |          |           |          |
| AdresseViti        | AlphaNum  |      255 | X             |           |          |           |          |
| CodePostalViti     | AlphaNum  |      255 | X             |           |          |           |          |
| VilleViti          | AlphaNum  |      255 | X             |           |          |           |          |
| TelephoneViti      | AlphaNum  |      255 | X             |           |          |           |          |
| IdentifiantTable   | AlphaNum  |      255 | X             |           |          |           |          |
| CapaciteTable      | Numérique |      255 | X             |           |          |           |          |
| IdentifiantBoisson | AlphaNum  |      255 | X             |           |          |           |          |
| DesignationBoisson | AlphaNum  |      255 | X             |           |          |           |          |
| prixVenteBoisson   | Numérique |          | X             |           |          |           |          |
| IdentifiantMenu    | AlphaNum  |      255 | X             |           |          |           |          |
| DesignationMenu    | AlphaNum  |      255 | X             |           |          |           |          |
| prixVenteMenu      | Numérique |          | X             |           |          |           |          |
| IdentifiantPlat    | AlphaNum  |      255 | X             |           |          |           |          |
| DesignationPlat    | AlphaNum  |      255 | X             |           |          |           |          |
| PrixPlat           | Numérique |          | X             |           |          |           |          |
| NumeroTypePlat     | AlphaNum  |      255 | X             |           |          |           |          |
| TypePlat           | AlphaNum  |      255 | X             |           |          |           |          |
| DatePriseCommande  |   Date    |          | X             |           |          |           |          |
| NumeroCommande     | AlphaNum  |      255 | X             |           |          |           |          |
| TypeService        | AlphaNum  |      255 | X             |           |          |           |          |

**2- Dépendances fonctionnelles**

a - DFP

IdentifiantEmploye -> (nomEmploye, prénomEmploye, adresseEmploye, CompAdresseEmploye, CodePostalEmploye, VilleEmploye, téléphoneEmploye, diplômeEmploye)

IdentifiantBout -> (DateAchatBout, PrixAchatBout)

IdentifiantVin -> (NomVin, MillesimeBout, PrixVenteBout)

IdentifiantViti -> (NomViti, PrenomViti, AdresseViti, CodePostalViti, VilleViti, TelephoneViti)

IdentifiantTable ->(CapaciteTable)

IdentifiantBoisson -> (DesignationBoisson, prixVenteBoisson)

IdentifiantMenu -> (DesignationMenu, prixVenteMenu)

IdentifiantPlat -> (DesignationPlat, PrixPlat)

IdentifiantTypePlat -> (DesignationTypePlat)

IdentifiantPlat -> TypePlat

IdentifiantCmd-> (DatePriseCommande,TypeService, sIdentifiantEmploye, NumTable)

(IdentifiantCmd, IdentifiantBoisson)-> qteBoisson
(IdentifiantCmd, IdentifiantVin)-> qteVin
(IdentifiantCmd, IdentifiantPlat)-> qtePlat
(IdentifiantCmd, IdentifiantMenu)-> qteBoisson


b - DFI

Explication:
Plat
| idPlat | libelle | prix |
| ------ | :-----: | ---: |
| 1      | Chourba |  250 |
| 2      | nachif  |  500 |
| 3      |  coca   |  500 |
| 4      | loubiya |  250 |
| 5      |  kibde  |  500 |
| 6      | salade  |  500 |

platMenu
| idPlat | idMenu |           date |
| ------ | :----: | -------------: |
| 1      |   5    | dateAujourdhui |
| 2      |   5    | dateAujourdhui |
| 3      |   5    | dateAujourdhui |
| 4      |   6    |       dateHier |
| 5      |   6    |       dateHier |
| 6      |   6    |       dateHier |

Menu
| idMenu | libelle | prix |
| ------ | :-----: | ---: |
| 5      |  BAMIA  | 1000 |
| 6      |  Menu2  | 3000 |

**3- MCD**

[Le MCD en pdf](../pdfs/mcd.pdf)

**4- MLD**

[Le MLD en pdf](../pdfs/mld.pdf)

# Etude de cas 2:

Vous avez été contacté par le directeur d'une bibliothèque municipale qui désire informatiser sa gestion. Il compte beaucoup sur la mise en place d'un système informatique pour améliorer la qualité du service offert aux usagers.

Actuellement, la gestion de la bibliothèque est faite entièrement manuellement, au moyen d'un système de fiches manuscrites. Ce système entraîne une charge de travail très lourde pour les employés et un gaspillage important (fiches périmées retirées du fichier). La lourdeur du système est évidente si l'on considère que la bibliothèque possède actuellement 36872 livres répartis entre 21709 titres différents et 2634 abonnés.

Grâce au système informatique, un abonné doit pouvoir retrouver un livre dans les rayons connaissant son titre. Les livres sont identifiés par un code catalogue qui leur est affecté à l'achat et par une cote qui permet de les situer dans la bibliothèque. L'abonné doit aussi pouvoir connaître la liste des livres d'un auteur ou la liste par éditeur ou encore la liste par thème (bande dessinée, science fiction, policier,...). Chaque livre est acheté en un ou plusieurs exemplaires (on stocke la date d'acquisition). Tous les exemplaires d'un même livre ont une cote différente mais le même code catalogue. Les différents exemplaires d'un même livre peuvent éventuellement provenir de différents éditeurs. Pour suivre de près l'état du stock, la bibliothèque utilise un code indiquant l'état d'usure de chaque livre. Ce code d'usure est éventuellement mis à jour par un bibliothécaire à chaque retour d'un livre en prêt.

Le directeur souhaite également mettre en place une procédure de recherche documentaire par mots-clés. Vous devez donc prévoir la possibilité de recherche à partir d'un mot-clé de tous les ouvrages correspondants. Un ouvrage peut avoir un nombre quelconque de mots-clés.

La bibliothèque utilise aussi un fichier des abonnés organisé par numéro matricule qui contient notamment les coordonnées (nom. adresse et téléphone) de l'abonné, sa date d'adhésion, sa date de naissance, sa catégorie professionnelle (ou bien étudiant ou enfant, le cas échéant).

La gestion des prêts implique qu'on connaisse à tout moment la liste des livres détenus par un abonné et inversement qu'on puisse retrouver le nom des abonnés détenant un livre non présent dans les rayons.

Les prêts sont accordés pour une durée de 15 jours éventuellement renouvelable, si aucune demande de ce livre n'a eu lieu entre-temps. IL faut donc connaître pour chaque livre emprunté, la date du prêt et la date de retour. La gestion des prêts nécessite aussi la mémorisation des livres demandés par un abonné. Cet abonné sera prioritaire lors du retour du livre en prêt. Sa priorité est maintenue pendant une semaine, à partir de la date de retour du livre.

**Travail à faire :**

- Établir un dictionnaire de données.
- Identifier les DF.
- Établir le Modèle Conceptuel de Données. 

// [Source](www.exelib.net): www.exelib.net

**Correction**

| Nom | Format | Longueur | T Elementaire | T Calculé | R.Calcul | R.Gestion | Document |
| --- | :----: | -------: | ------------- | --------- | -------- | --------- | -------- |
|     |        |          |               |           |          |           |          |





