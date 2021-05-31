# Leçon 5: Verification du model: Les formes normales
<u>Proverbe</u>« The key, the whole key, nothing but the key » 

Pour eviter les anomalies de: <br>
1- Lecture (pertes des données)<br>
2- Ecriture<br>
3- Redondance des données<br>
4- Contre-performance.<br>

## I - Prémiere forme normale (1FN => 1FN = La clé)

Une relation est en 1FN si
* tous ses attributs sont atomiques
* ses attributs ne sont repétés

## II - Deuxième forme normale (2FN => 2FN = Toute la clé)
Une relation est en 2FN si
* elle est en 1FN
* tous ses attributs non cle ne dependent pas d'une partie de sa clé primaire.

## III - Troisième forme normale (3FN => 3FN = Rien que la clé)

Une relation est en 3FN si
* elle est en 2FN
* toutes les dépendances fonctionnelles % à la cle sont directes.

## IV - Forme normale de Boyce Codd (FNBC)

Une relation est en FNBC si
* elle est en 3FN
* Les seules dépendances fonctionnelles sont celles dans lesquelles une clé determine un attribut.

## V - Quatrième forme normale (4FN)

Une relation est en 4FN si
* elle est en BCNF
* Lorsqu'il existe une dependance multivaluée élémentaire.

## VI - Cinquième forme normale (5FN)

Une relation est en 5FN si
* elle est en 4FN
* Elle ne possede pas de dépendance de jointure

## VII - Forme normale domaine clé (FNDC)
Une relation est en FNDC si
* elle est en 5FN
* Toutes les contraintes sont la conséquence logique des contraintes de domaines et des contraintes de clés qui s’appliquent à la relation.


## VIII - Sixième forme normale (6FN) : moins importante

