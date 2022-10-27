# Configuration

Pour configurer votre équipement il faut se rendre dans l'onglet du plugin Suivi Conso.<br>
_**Plugins / Energie / Suivi Conso**_ <br>

Cliquer sur "Ajouter un équipement" <br>
![ecq](../images/ecq.png)



**Libelle** : Nom de votre équipement <br>

**Type** : Electricité ou Prod. Elect. ou Gaz ou Fioul ou Eau<br>

**Objet Parent** : renseigner la catégorie de votre équipement. <br>

**Equipement parent** : Permet de rattacher un équipement à  un parent afin de récupérer les informations du père. <br>

**Compteur**: Puissance maximale pouvant être atteinte. La graduation de la jauge de puissance dépend de cette information. Pour les sous-équipemnts il y a la possibilité de définir un maximal différent.

**Informations récupérées du parent :**
 - Abonnement
 - Compteur/Puissance (par défaut, mais modifiable tout de même pour les sous-équipements pour régler l'échelle de la jauge. Pour cela cocher la case "Puissance personnalisée")
 - Type
 - Commande PTEC
 - Commande IMAX

**Abonnement :** Le type de tarif actuellement géré. Bleu(Heure pleine heure creuse),Base (heure pleine) <br>

**Production complémentaire :** Lorsqu'une hiérarchie parent enfants (équipement principal, sous-équipement) existe, un graphe camembert de la répartition des consommations apparait. Si la somme de la consommation des enfants dépasse celle de l'équipemnt parent, alors un message d'erreur apparaitra. Si jamais on place en tant que sous équipement la production solaire alors pause le problème puisque la somme de cconsommation dépassera l'équipement parent. Cette cas s'il est cochée permet de passer outre ce problème.<br>

**Je n'ai que la consommation de mon équipement (Exemple FGD-212)  :** <br>
 - Commande disponible : <br>
 - Consommation Kwh ou Wh <br>
 - Puissance PAPP

**je n'ai que la puissance de mon équipement (Exemple FGD-211) :** <br>
Commande disponible : <br>
 - Etat : Votre équipement est allumé ou éteint (Type : numerique 0 ou 1 ) <br>
 - Consommation électrique déclarée  (Wh) La consommation de vos ampoules ou équipements une fois mesurée

 ## Si un parent a été attribué :

 **Application Abonnement :**<br>
 Permet d'applliquer l'abonnement sur l'équipement enfant.<br>

 **Puissance personnalisée :**
 Si coché remplace le champ _**Compteur**_ par le champ _**Puissance**_ :
 - Si le champ est vide alors la jauge sera automatique. Elle prendra la valeur max de la journée qu'elle arrondira au kVa superieur et l'appliquera à la jauge.
 - Si vous spécifiez une valeur, la jauge se configura par rapport à votre valeur.


Si votre équipement est un total cocher la case Total. <br>
Le bouton Défaut permet d'afficher un équipement au démarrage de votre panel.<br>
Ces deux cases ne sont disponibles que pour les équipements qui n'ont pas de parent.<br>

Une fois les informations renseignées, il faut ajouter les commandes nécessaires au bon fonctionnement du plugin . <br>
Pour cela cliquer sur _**Ajouter les commandes**_ <br>

![add_cmd](../images/add_cmd.jpg)


Pour sélectionner les commandes il faut cliquer sur la pastille verte ou orange pour récupérer les informations . <br>
![configuration](../images/configuration.jpg)



Puis il vous faut récupérer les commandes configurées dans Jeedom. <br>
![commandes](../images/commandes.jpg)
