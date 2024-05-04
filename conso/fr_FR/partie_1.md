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

**Abonnement :** Le type de tarif actuellement géré. Bleu(Heure pleine, heure creuse), Base (heure pleine), Tempo (heure pleine, heure creuse) <br>

**Production complémentaire :** Lorsqu'une hiérarchie parent enfants (équipement principal, sous-équipement) existe, un graphe camembert de la répartition des consommations apparait. Si la somme de la consommation des enfants dépasse celle de l'équipement parent, alors un message d'erreur apparaitra. Si jamais on place en tant que sous équipement la production solaire, alors cela pause un problème puisque la somme des consommations dépassera celle de l'équipement parent. Cette case, si elle est cochée permet de passer outre ce problème.<br>

**Je n'ai que la consommation de mon équipement (Exemple FGD-212)  :** <br>
Généralement sur Non pour la teleinfo et sur sur Oui pour les équipements type Fibaro Wall plug <br>
Commande disponible : <br>
 - Consommation avec choix de l'unité (kWh ou Wh) <br>
 - Variation max autorisée entre 2 mesures: Permet d'éviter de fausser les relevés en cas de pics de consommation survenu par erreur.
 - Puissance PAPP
 - PTEC (On attends HPJB, HCJB, HPJW, HCJW, HPJR, HCJR pour Tempo; HP, HC pour un tarif HP/HC; HP pour le tarif Base).
 Pour ceux qui possède un Zlinky pour adapter l'info à ce que le plugin attend en tarif TEMPO, il faut renseigner comme ceci:
```sql
 (#[Consommations][ STD][LTARF]# == "HP  BLEU"?"HPJB":(#[Consommations][ STD][LTARF]# == "HC  BLEU"?"HCJB":(#[Consommations][ STD][LTARF]# == "HP  BLANC"?"HPJW":(#[Consommations][ STD][LTARF]# == "HC  BLANC"?"HCJW":(#[Consommations][ STD][LTARF]# == "HP  ROUGE"?"HPJR":"HCJR")))))
 ```
 En remplaçant la commande #[Consommations][ STD][LTARF]# par la votre. Attention aussi en générale il y a 2 espaces entre HP et BLEU et de même pour les autres couleurs
 - INST1 (Intensité instantanée)
 - IMAX1 (Intensité maximale atteinte) On peut choisir d'avoir l'intensité maximale absolue ou bien celle de la journée. Il faut alors historiser la commande utilisée et renseigner le champ avec une commande telle que : maxbetween(#[Consommation][Teleinfo 1][Intensité instantanée]#, midnight,now)
 - température extérieure


**je n'ai que la puissance de mon équipement (Exemple FGD-211) :** <br>
Il faut fournir l état de l équipement et la consommation électrique déclarée.<br>
Commande disponible : <br>
 - Etat : Votre équipement est allumé ou éteint (Type : numerique entre 0 et 1. Pour une lumière allumé à 60% il est possible de mettre 0.6. Cela permettra de ne comptabiliser que 60% de la "puissance électrique déclarée"). On peut mettre 1 en fixe, si on considère que l'équipement consomme tout le temps et que la "puissance électrique déclarée" varie <br>
 - Consommation électrique déclarée  (Wh) La consommation de vos ampoules ou équipements une fois mesurée. On peut mettre une valeur fixe qui correspond par exemple à la consommation d'une ampoule, et alors la puissance comptabilisé dépendra alors de l'état (0: aucune consommation, 1: consommation maximale, entre 0 et 1: consommation au prorata de la valeur. Exemple si 0.6 alors puissance consommée = Consommation électrique déclarée * 0.6)

**Enregistrement de la consommation à J-1 :** <br>
 Ce paramétrage est dédié à l'utilisation des plugin type Enedis ou Gaspar qui remontent le jour J l'information de consommation de la veille. Cela permet d'enregistrer la consommation sur la date de la veille. En cas d'utilisation il n'y aura donc aucune information sur le jour en cours dans les graphiques et dans les tableaux de consommation/prix.

**Catégories :** <br>
 Elles servent quand une hiérarchie père enfants existe. (Exemple: père: consommation de la maison, enfants: consommation du chauffage, consommation de la lumière ...). Elles servent pour l'affichage d'un camembert de répartition des consommation dans le tableau Statisitique. Elles ne sont utiles que pour les enfants dans la hiérarchie. Elles permettent de regrouper plusieurs équipement. Par exemple si on a 2 équipements pour la lumière (Salle à manger, Cuisine), en cliquant la catégorie "lumière", cela permettra d'avoir une seul rubrique lumière dans le camembert représentant les 2 lumières salle à manger et cuisine.
 Dans le cas où aucune case n'est cochée sur l'enfant, alors ce sera le libellé de l'équipement qui apparaitra dans le camembert.
 Il peut y avoir plusieurs niveaux de hiérarchie. Le camembert affiché concernera alors le niveau de l'enfant sur lequel on se trouve.<br>.<br>
 ![Hierarchie](../images/Hierarchie.png)<br><br>
 ![Statistique_fils](../images/Statistique_fils.png)<br><br>
 ![Statistique_petit_fils](../images/Statistique_petit_fils.png)<br>

 Une catégorie "indéfinie" apparaitra automatiquement dans le camembert. Elle représente l'écart entre la consommation du père et la somme de consommation des enfants. Elle représente donc la partie détaillée non mesurée de la consommation.

 _**Exemple**_: Il peut être interressant de l'utiliser pour calculer son taux d'autoconsommation quand on possède des panneaux solaires. Il suffit alors de mesurer la consommation globale de la maison en tant que père et d'ensuite renseigner un enfant qui récupèrera la teleinfo du compteur Linky (représentant sa consommation). Le camembert donnera alors le taux d'autoconsommation dans la catégorie "Indéfinie" qui sera en réalité ce que la maison a consommée à partir de la production solaire.

# Important :
 _**Si la somme de la consommation des enfants est supérieure à celle du père, le camembert ne s'affichera pas. Le moyen de passer outre cela est de cocher la case "Production complémentaire" au niveau du paramétrage de l'équipement père pour indiquer que l'on produit plus que ce que l'on consomme.**_


## Si un parent a été attribué :

 **Application Abonnement :**<br>
 Permet d'appliquer l'abonnement sur l'équipement enfant.<br>

 **Puissance personnalisée :**
 Si coché remplace le champ _**Compteur**_ par le champ _**Puissance**_ :
 - Si le champ est vide alors la jauge sera automatique. Elle prendra la valeur max de la journée qu'elle arrondira au kVa superieur et l'appliquera à la jauge.
 - Si vous spécifiez une valeur, la jauge se configura par rapport à votre valeur.

**Total**
Si votre équipement est un total cocher la case Total. <br>
Cela permettra de faire apparaître le camembert de répartition des consommations si des équiepements enfants sont liés

**Défaut**
Le bouton Défaut permet d'afficher un équipement au démarrage de votre panel.<br>
Si plusieurs équipements ont la case "Défaut" de cocher alors celui affiché sera celui dont l'ordre alphabétique du nom est le preier

Ces deux dernières cases ne sont disponibles que pour les équipements qui n'ont pas de parent.<br>

Une fois les informations renseignées, il faut ajouter les commandes nécessaires au bon fonctionnement du plugin . <br>
Pour cela cliquer sur _**Ajouter les commandes**_ <br>

![add_cmd](../images/add_cmd.jpg)


Pour sélectionner les commandes il faut cliquer sur la pastille verte ou orange pour récupérer les informations . <br>
![configuration](../images/configuration.jpg)



Puis il vous faut récupérer les commandes configurées dans Jeedom. <br>
![commandes](../images/commandes.jpg)
