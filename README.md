## Groupe Laforge Douillard Kristensen

**application en fonctionnement :** https://dogwood-abacus-300711.appspot.com/indexPet.html#!/home

**Fonctionnalités demandées :**
- Create a petition: On peut créer une petition ayant un nom et un sujet rattaché (un "tag")
- Sign a petition (cannot sign two times, and better if users are authenticated) : Un utilisateur peut signer une pétition, on vérifie dans la liste des signataires si le mail de la personne authentifiée est présent ou non et on l'ajoute si besoin
- List petitions  signed by a user triées par date: Sur la page "Mes pétitions" on récupère les pétitions signées par l'utilisateur connectée (par défaut si on crée une pétition on est inclu dans les signataires) le tri se fait via la clé. On affiche 5 pétitions par 5 pétitons.
- List top100 petitions triées par date : Sur la page home on charge les pétitions par nombre de signataire, le tri par date se faire via la clé, on peux ensuite filtrer par thème de pétitions. On affiche 5 pétitions par 5 pétitons.
- (optional) tag petition/find petition by tag triée par date de création : On a pour le moment un tag par pétition pour trier plus facilement parmis les pétitions du top 100.

**Shema de données :**
![image](https://user-images.githubusercontent.com/45417431/117510356-3a1a0c80-af8c-11eb-89bb-a858b26e2893.png)

**Ce qui pourrait être amélioré :**
 - Implémenter plusieur tags par pétition pour permettre un filtrage plus précis
 - Ne pas importer la liste des signataires lors du chargement, d'où la limite pour le moment du chargement de 5 pétitions par "page" afin de limiter le temps de chargement même avec un certain nombre de signataires.
 - Trouver un moyen plus optimiser de savoir si l'utilisateur à déjà signé que charger la pétition et vérifier les signataires, pour vérifier directement dans la requête et pas dans le endpoint.
