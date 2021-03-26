**Énoncé :**

Vous avez été contacté par le directeur d'une bibliothèque municipale qui désire informatiser sa gestion. Il compte beaucoup sur la mise en place d'un système informatique pour améliorer la qualité du service offert aux usagers.

Actuellement, la gestion de la bibliothèque est faite entièrement manuellement, au moyen d'un système de fiches manuscrites. Ce système entraîne une charge de travail très lourde pour les employés et un gaspillage important (fiches périmées retirées du fichier). La lourdeur du système est évidente si l'on considère que la bibliothèque possède actuellement 36872 livres répartis entre 21709 titres différents et 2634 abonnés.

Grâce au système informatique, un abonné doit pouvoir retrouver un livre dans les rayons connaissant son titre. Les livres sont identifiés par un code catalogue qui leur est affecté à l'achat et par une cote qui permet de les situer dans la bibliothèque. L'abonné doit aussi pouvoir connaître la liste des livres d'un auteur ou la liste par éditeur ou encore la liste par thème (bande dessinée, science fiction, policier,...). Chaque livre est acheté en un ou plusieurs exemplaires (on stocke la date d'acquisition). Tous les exemplaires d'un même livre ont une cote différente mais le même code catalogue. Les différents exemplaires d'un même livre peuvent éventuellement provenir de différents éditeurs. Pour suivre de près l'état du stock, la bibliothèque utilise un code indiquant l'état d'usure de chaque livre. Ce code d'usure est éventuellement mis à jour par un bibliothécaire à chaque retour d'un livre en prêt.

Le directeur souhaite également mettre en place une procédure de recherche documentaire par mots-clés. Vous devez donc prévoir la possibilité de recherche à partir d'un mot-clé de tous les ouvrages correspondants. Un ouvrage peut avoir un nombre quelconque de mots-clés.

La bibliothèque utilise aussi un fichier des abonnés organisé par numéro matricule qui contient notamment les coordonnées (nom. adresse et téléphone) de l'abonné, sa date d'adhésion, sa date de naissance, sa catégorie professionnelle (ou bien étudiant ou enfant, le cas échéant).

La gestion des prêts implique qu'on connaisse à tout moment la liste des livres détenus par un abonné et inversement qu'on puisse retrouver le nom des abonnés détenant un livre non présent dans les rayons.

Les prêts sont accordés pour une durée de 15 jours éventuellement renouvelable, si aucune demande de ce livre n'a eu lieu entre-temps. IL faut donc connaître pour chaque livre emprunté, la date du prêt et la date de retour. La gestion des prêts nécessite aussi la mémorisation des livres demandés par un abonné. Cet abonné sera prioritaire lors du retour du livre en prêt. Sa priorité est maintenue pendant une semaine, à partir de la date de retour du livre.


**Travail à faire :**

- Établir un dictionnaire de données.
- Identifier les règles de gestion.
- Établir le Modèle Conceptuel de Données. 
- Déduire le Modèle Relationnel de Données. 


// [Source](www.exelib.net): www.exelib.net