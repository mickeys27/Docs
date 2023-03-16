## V3.30
- Forcer l'affichage des graph TEMPO en stack quand un historique est présent
- Améliorer visibilité température dans graphe du jour

## V3.29
- Correction graph jour dans partie mobile
- Changement couleur tarif Tempo Bleu HP

## V3.28
- Correction problème libellé total dans facture pour le gaz et le fuel
- Bug de prise en compte du nombre de kWh dans les taxes pour le tarif TEMPO
- Correction des couleurs graphes et tableau variation pour TEMPO
- Correction affichage des valeurs dans les graphes pour le gaz et le fioul

## V3.27
- Permettre de visualiser les camemberts sur les sous-niveaux quand plus de 2 niveaux de hiérarchie

## V3.26
- Ajout camembert année-1
- Possibilité d'afficher systématiquement la température dans le graphe consommation du jour (Paramétrage dans la configuration du plugin)
- Renommage de l'étiquette de la courbe puissance sans le graphe consommation du jour
- Ajout Tarif Tempo
- Changer l'ordre des factures du plus récent au plus ancien

## V3.25
- Préparation base de données pour tarif Tempo 2ème partie (L'installation peut être un peu long suivant la taille des tables)

## V3.24
- Préparation base de données pour tarif Tempo (L'installation peut être un peu long suivant la taille des tables)

## V3.23
- Inclure la table conso_jour pour le bouton changement d'ID équipement
- Agrandissement champs inst1 et imax1 de la table conso_teleinfo pour les installations pro

## V3.22
- Mise à jour suite au changement du core v4.x
- Ajout camembert de la Veille
- Ajout catégorie Domotique

## V3.21
- Ajout catégories Piscine et Climatisation
- Remplacement catégorie Autres automatique par la catégorie Indéfini

## V3.20
- Corrections arrondi diverses
- Mise à jour documentation
- Ajout info type tarif hors taxe
- Correction widget partie mobile

## V3.19
- Correction arrondi partie fixe dans graphe TTC 12 mois

## V3.18
- Correction position résumé
- Correction affichage bouton de sélection fenêtre saisie périodes, prix, abonnements, taxes, TVA
- Ajout graphes pluri-annuels
- Historisation et épuration automatique table conso_teleinfo
- Ajout de la possibilité d'enregistrer les consommations à J-1 (exemple si utilisation plugin ENEDIS)

## V3.17
- Ajout de la version du plugin dans le panel
- Correction affichage résultat bouton tester dans config équipement
- Correction facture

## V3.16
- Amélioration lecture tooltip complexe
- Problème icones sur page configuration

## V3.15
- Ajout sous-catégorie Matériel Informatique
- Corrections pour version Jeedom v4.2

## V3.14
- Correctif taille tooltip
- Correctif conso 1ère semaine an-1 du graphe 4 semaines
- Correctif valeur commande pour le gaz et tableau prévisions

## V3.13
- Fix icones infos en V4
- Correction date graphe semaine si semaine 53 dans l'année
- Fix error javascript
- Correction erreur images structure table panel sauvegarde
- Debug panel mobile
- Optimisation nombre de commande équipement
- Amélioration intitulé commandes Eau, gaz, fioul
- Maj des unités par défaut des commandes
- Correction relevés commandes saisons
- Suppression contrôle Papp négatif
- Ajout contrôle sous-équipement ne soit pas lui-même

## V3.12
- Correction absence PTEC en mode je n'ai que la puissance de mon équipement
- Ajout commandes J-2, S-1, S-2, M-1, M-2, A-1, A-2, saisons, J-7  glissant, J-15 glissant, J-31 glissant
- Correction icône poubelle en V4
- Correction fonctionnement suppression sur table jour dans Configuration/Données


## V3.11
- Correction mode VARIATION : Insère si Conso > Conso précedente
- Corrections diverses
- Update Tag V4 Market et tri des fichiers

## V3.10
- Correction valeur 1ère semaine sur graphe 4 semaines
- Ajout du tableau prévisions pour les équipement type eau, fioul et gaz.
- Ajout d'un filtre paramétrable à l'équipement (type FGD-212) pour ne pas enregistrer que les consommations qui dépassent le seuil renseigné
- Correction des bornes de sélection pour le correcteur
- Ajout informations données au survol dans les graphes.
- Correction libellé pour la puissance en paramétrage type FGD211
- Correction partielle problème mode VARIATION : Insère si Conso > Conso précedente

## V3.9
- Bugfix anomalies de la version 3.8

## V3.8
- Suppression de l'unité dans les graphiques pour avoir toutes les données affichées
- Correction de la commande abonnement en cours
- Correction pour le cumul des catégories dans le camembert si plusieurs équipements avec une même catégorie
- Autorisation de prendre la somme des sous-équipements comme somme totale de la consommation si celle-ci est supérieure au père pour le camembert

## V3.7
- Correction des pourcentages sur le panel Prévisions
- Camembert statistique: Correction des pourcentages HP/HC pour la catégorie "Autres".
- Ajout d'une catégorie Véhicules pour la répartition des consommation (Il faut resauvegarder tous les équipements)
- Amélioration du choix des noms des catégories dans le camembert.
- Alerte et effacement du camembert quand la somme des sous-équipements est supérieure à l'équipement total.
- Correction intitulé de la valeur à saisir dans la cas d'un équipement avec choix FGD-211
- Ajout d'une api pour que les développeurs puissent intéragir avec les données du plugin
- Ajout d'un onglet avec tous les plugins partenaires
- Correction calculs graphiques, statistiques, factures pour les paramétrages avec impulsion différent de 1
- Différentier par une icone différente les parents des enfants
- Ajout d'une commande avec le prix en cours
- Correction du chemin pour l'import
- Correction de la fonction de téléchargement des fichiers de paramétrages
- tri des données dans le tableau des taxes
- Correctif pour en tarif de base ne pas faire apparaître les lignes HC dans les factures
- gestion du nombre de décimales sur la tableau des consommations
- Correctif pour faire saisir les 2 prix HC et HP dans les catégories électricité et production, même si un équipement est en heure base.
- Dans la saisie des prix, suppression de la confirmation du prix pour l'eau et le gaz
- Ajout de boutons "tester" pour vérifier les commandes appliquées au paramétrage d'un équipement
- Ajout des températures au relevé de gaz et du fioul

## V3.6
- Correction de la perte de donnée à la désactivation du plugin
- Correction d'un bug sur les version des thèmes
- Ajout des abonnnement uniquement sur l'équipement Total
- Correction du thème V3 Default
- Suppression du message "Pour visualiser le graphique merci de renseigner la Puissance instantanée" pour les équipements autres que électricité et production
- Ajout gestion de catégorie, gaz, fioul, production d’électricité (taxe non obligatoire)
- Correction de l'export global en csv
- En cas de redémarrage du plugin faire en sorte de ne pas perdre les paramétrages prériodes, prix, abonnement, etc ...
- Ajout d'une option pour ne pas prendre en compte l'abonnement pour les sous-équipements
- Arborescence des équipements dans le menu
- Trie par catégorie dans le paramétrage des équipements
- Option pour jauge adaptable en fonction de la puissance et avec une valeur mini à 1kW, ou bien saisie libre de la puissance
- Suppression visibilité case à cocher defaut et total pour les sous-équipements. Et forçage à décocher par défaut pour les sous-équipements.
- Cacher la case PTEC dans la config en tarif base
- Amélioration compatibilité php 7.3
- Ajout de la synthèse des statistiques pour la catégorie eau et les nouvelles catégories
- Ajout de la possibilité de sélectionner la devise.

## V3.5
- Gestion thème en fonction de la version Jeedom (V3 ou V4)
- Ajout synthèse statistiques pour l'eau
- Remise en HT des commandes Prix TOTAL
- Ajout des commandes Prix TTC HC, Prix TTC HP, Prix TTC TOTAL
- BugFix tableau prévisions pour l'année
- BugFix lien documentation
- BugFix des points manquants pour les années - 1 dans les graphiques
- Bugfix du décalage d'heure dans les historiques Jeedom
- Amélioration présentation des valeurs dans les graphiques

## V3.4
- Ajout d'informations dans la version mobile
- Compatibilité Jeedom V4
- BugFix de la version Mobile
- BugFix des thèmes en V4
- BugFix abonnement sur facture pour période courte
- BugFix tableau des variations

## V3.3
- Le dashboard pour l’eau a été peaufiné
- le panel prix correspond au centimes près au graphique TTC sur 12 mois et aux statistiques
- Les factures Electricité et Eau fonctionnent correctement.
- Gestion des dates d'application des taxes et des prix hors périodes de calcul. Entrez celles de votre facture réelle.
- Il est possible de saisir plusieurs prix différents pour une même période (nécessaire notamment pour l’eau)


## V3.2
- Ajout page de correction des données
- Mise en place des commandes.
- Mise a jour de la documentation
- Nouvelle présentation dans la configuration
- Correction affichage 12 derniers mois TTC


## V3.1
-Correction bug compteur eau

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
-Ajout d'un bouton "Identifier les erreurs" dans l'onglet outils
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
-Possibilité d'importer ou d'exporter une configuration dans l onglet Save.
-Correction affichage firefox des températures


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
- Popup periode enlever la scrollbar +
- Masquer bouton "ajouter" equipement si > 0 +
- J'arrive pas a supprimer des lignes dans l'onglet prix. Ils disparaissent bien mais quand tu reviens dessus plus tard ils sont de nouveau la. +
- Harmonisation Ajout et suppression d'une donnée. +
- CREATION DE LA DOC +
- Position valeur MIn et Min +
- Couleur Valeur Max et Min +

## V1
- Supprimer ligne de code mysql dans la conf +
- Ajouter le prix de lâ€™abonnement. +
- Ajouter la puissance souscrite +
- Expliquer dans l equipement les entrees +
- Faute dans gestion de la TVA +
- Forcer visible a non puis masquer le champ dans equipement +
- Quand on rajoute une période il serait bien que dans les options d'affichage lorsque on est sur non il soit en rouge c'est un détails mais plus clair. +
- Corrections des onglets tva ,taxe,prix update ,delete , add +
- Affichage consommation de la veille correction de la semaine lorsque la date du jour = dimanche parametrage de l abonnement pour la gauge +
- Correction bug tableau vide correction de valeur a 0 sur les graphs HP HC OLD +
- Table sauvegarde lors de la purge +
- Ajout logs modification des couleurs corrections notices +
- Ajout d un onglet abonnement +
- Ajout d un onglet Info Il permet de visualiser les tables de gestion teleinfo et jour +
- Refonte du popup détail refonte du tooltips quand la souris passe sur un graphique du dashboard. +
- Ajout du minimum sur la trame du jour +
- Correction et modification affichage des libellés sur les graphs du dashboard. +
- Ajout d un bouton synchroniser aujourd'hui dans outil permet de synchroniser la ligne du jour dans la table jour en cas d erreur +
- Affichage de la legende + gauge sur la trame du jour - Couleur onglet - prise en charge abonnement de base +
- Modification de la gestion des taxes modifications des libelles +
- Si pas année-1 alors on masque la legende +
- Correction sql +
