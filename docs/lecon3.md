# Leçon 4: Model logique des données

## I - Régles de passage

### Cas n°1 : many to one
c'est le cas (0,n) <--> (1,1) ou (1,n) <--> (0,1)
* Supprimer la rélation
* L'entité (1,n) ou (0,1) absorbe l'identifiant de l'entité la plus forte(l'autre entité). C'est à dire ajouté une clé étrangere. 
Cas particulier: les associations reflexives.

### Cas n°2 : many to many
C'est le cas (0,n) <--> (0,n) ou (1,n) <--> (1,n)
* Transformer la rélation en entité (C'est à dire même nom et si la relation est porteuse, les propriétés de la relation deviennent les propriétés de la nouvelle entité)
* Cette nouvelle entité absorbe les identifiants des autres entités. 
* La clé primaire de la nouvelle entité est la concaténation des clés primaires des autres entités. 

## II - [Etude de cas:](exercice.md)
Mettre en place le MLD pour l'étude de cas n°1 et à partir du MCD existant.