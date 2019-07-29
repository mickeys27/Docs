## V3.2
- Ajout page de correction des données
- Mise en place des commandes.
- Mise a jour de la documentation
- Nouvelle présentation dans la configuration
- Correction affichage 12 derniers mois TTC


## V3.1
- Correction bug compteur eau

## V2.14
- Configuration du plugin : VARIATION : Insere uniquement si la consommation est > 0
- Configuration du plugin : PUISSANCE : Ne pas insérer la valeur si la puissance est > 50 000
- Corrections des previsions

## V2.13
- BugFix Tache cron introuvable
- BugFix Editer/Supprimer des données du tableau téléinfo dans l'onglet Données

## V2.12
- Compatible Jeedom V3

## V2.11
- Correction erreur $mode non definie sur la page de configuration des temperatures

## V2.10
- Correction pour Docker
- Correction du graphique 7 derniers jours pour l'equipement Eau
- Correction date de debut de facture ( ajout du jour )
- Correction de la date de prévision
- Correction erreur log
- Correction orthographe

## V2.9
- Correction graphique 4 dernières semaines
- Sécurite si un equipement est père d'un autre et qu'il est supprimé.
- Correction des graphiques sous forme de camembert.
- Mise en place des previsions si un historique de plus d'un an existe.
- Ajout log conso_erreur ( generation des requetes SQL de correction pour les grosse variations a cause d un module en erreur)
- Prise en compte des equipements sans consommation , Seul la puissance et l'etat seront nécéssaires ( exemple FGD-211)
- Affichage de la taille de la table des données dans l'onglet Save


## V2.8
- Correction graphique 4 dernières semaines
- Correction graphique 12 derniers mois

## V2.7
- Correction affichage block rouge avec messages erreurs lorsqu'il n'y a pas assez de données.
- Ajout securite pour les equipements avec une consommation instable.

## V2.6
- Correction graphique DJU par année
- Correction du mode de chauffage dans onglet température
- Securite sur les equipements sans index ( Ã  consommation seulement )
- Correction libelle kWh
- Drapeau masqué si la commande n'est pas configuré.
- Correction des logs

## V2.5
- Parametrage de l'unité utilisée ( Kwh ou Wh)  par les equipements type fibaro

## V2.4
- Les dates de configuration sont bloqué a 2037 max
- Affichage DJU en fonction du mode : chauffage ou clim
- Graphique 12 derniers mois TTC en fonction de la date de la facture (onglet outils)
- Correction calcul DJU
- Amélioration de la feuille de style
- Correction bugs lors de la sauvegarde des parametres ( onglet Save )
- Correction tableau variations
- Correction export des paramatres

## V2.3
- Ajout d'un bouton "Identifier les erreurs" dans l'onglet outils
Ce bouton permet de retrouver les index inférieurs au premier index inséré dans la base
Si un relevé ( hp ou hc )  est inférieur premier relevé alors il est considéré comme une valeur fausse.
- Correction du calcul du DJU ( ne prend plus la température 0 qui correspond a une erreur de relevé)
- Correction bug sur les factures
- Tableau de synthèse refonte
- Correction bug sur le montant total du tableau en page d accueil
- Dans outils , possibilité de paramatrer la période du calcul de l'année  (Tableau de consommation de la page d'acceuil )
- Ajout d'un logo (i) dans les tableaux en page d'acueil pour afficher la periode.
- Affichage du DJU :
12 derniers mois
4 dernières semaines
7 derniers jours
- Possibilité d'importer ou d'exporter une configuration dans l onglet Save.
- Correction affichage firefox des températures


## V2.2
- Correction de la vue mobile
- Affichage du prix TTC dans le tableau de synthèse
- Correction affichage Fermerture dans la dialogBox ( Popup )
- Correction affichage du bouton Enregistré dans les dialogBox ( Popup )
- Ajout du graphique température min max et moyenne derriere les graphiques de consommation en Kwh ( cliquer sur l'icone en bas a droite du graph )
- Ajout du graphique DJU sur la page d'accueil (Degré jour unifié par an)
- Ajout de la page configuration / température  DJU (Degré jour unifié par an)
- Correction sur le calcul des taxes dans le tableau de la page d'accueil si plusieurs taxes sont configurées selon une date

## V2.1
A minuit :
- Insertion de la donnée a 23h59 du jour
- Insertion de la donnée a 00h00 du lendemain

- Correction du tableau consommation en eau ( M3 et L )
- Modification du libelle dans la config de l'équipement Eau : ( Compteur -> Nombre dâ€™impulsion au total )
- Unité ajoutée dans le paramétrage de la commande
- Tableau synthèse ajout du Total TTC
- Correction de la roue crantée @nanard54
- avertissement si aucun prix n est configuré a la date du jour
- correction de la fonction "purger"

## V2.0
- !!!!!!!!!!! Gestion du multicommande !!!!!!!!!!
- Gestion du compteur Eau
- Ajout du type Abonnement  ( electricité ou eau )
- Ajout du type de periode  ( electricité ou eau )
- Ajout du type de prix  ( electricité ou eau )
- Ajout du type de taxe  ( electricité ou eau )
- Changement Id equipement (permet de modifier l id equipement vers un autre ID equipement ) dans outils
- Supprimer  les données d' un équipement ( dans outils)
- Correction d affichage des tableaux
- Corrections des retours de bugs utilisateurs
- Onglet : Outils, Configuration et Save visible uniquement en mode Expert
- Graphique du jour : possibilité de selectionner la periode
- Refonte des bloques bootstrap du panel
- Possibilité d ajouter une bouton retour dans le menu ( dans outils )
- Modification de l interface configuration
- Mise a jour Doc

## V1.3
- Ajout de la température
- Infobull dans les 2 tableaux sur l'accueil
- Correction bug a l installation ( id_tva )
- Modification du menu
- Sauvegarde des données
- Import des données
- Import des donnes depuis un serveur distant
- Modification et  suppression des données depuis la page info
- Modification de la gestion de la table jour
- Plus besoin de garder l historique de la table teleinfo , il faut seulement les 2 derniers jours pour le graphique du jour de l accueil.
- La table jour ne se vide plus, les données sont remplacées lors de la synchro.
- Suppression des champs non utilisés dans la table téléinfo.
- Correction affichage tableau variation
- Correction bug lors de l edition d une taxe , periode et TVA


## V1.2
- Popup periode enlever la scrollbar 
- Masquer bouton "ajouter" equipement si > 0 
- J'arrive pas a supprimer des lignes dans l'onglet prix. Ils disparaissent bien mais quand tu reviens dessus plus tard ils sont de nouveau la. 
- Harmonisation Ajout et suppression d'une donnée. 
- CREATION DE LA DOC 
- Position valeur MIn et Min 
- Couleur Valeur Max et Min 

## V1
- Supprimer ligne de code mysql dans la conf 
- Ajouter le prix de lâ€™abonnement. 
- Ajouter la puissance souscrite 
- Expliquer dans l equipement les entrees 
- Faute dans gestion de la TVA 
- Forcer visible a non puis masquer le champ dans equipement 
- Quand on rajoute une période il serait bien que dans les options d'affichage lorsque on est sur non il soit en rouge c'est un détails mais plus clair. 
- Corrections des onglets tva ,taxe,prix update ,delete , add 
- Affichage consommation de la veille correction de la semaine lorsque la date du jour = dimanche parametrage de l abonnement pour la gauge 
- Correction bug tableau vide correction de valeur a 0 sur les graphs HP HC OLD 
- Table sauvegarde lors de la purge 
- Ajout logs modification des couleurs corrections notices 
- Ajout d un onglet abonnement 
- Ajout d un onglet Info Il permet de visualiser les tables de gestion teleinfo et jour 
- Refonte du popup détail refonte du tooltips quand la souris passe sur un graphique du dashboard. 
- Ajout du minimum sur la trame du jour +
- Correction et modification affichage des libellés sur les graphs du dashboard. 
- Ajout d un bouton synchroniser aujourd'hui dans outil permet de synchroniser la ligne du jour dans la table jour en cas d erreur 
- Affichage de la legende + gauge sur la trame du jour - Couleur onglet - prise en charge abonnement de base 
- Modification de la gestion des taxes modifications des libelles 
- Si pas année-1 alors on masque la legende 
- Correction sql 

