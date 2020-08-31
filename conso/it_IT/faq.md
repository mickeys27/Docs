# FAQ du plugin Suivi Conso

## Il me manque des informations HP/HC/PTEC
S il vous manque des informations, que vous ne pouvez pas récupérer, le tuto vous permettra de les simuler.

L'objectif de ce tuto est d'utiliser le Plugin sans les informations remontées par la teleinfo.
S il vous manque : PTEC , index ... 

[Voir le Tuto](./tutoriel_hp_hc.md)

## Questions Fréquentes

### Je ne trouve pas le Widget dans le Dashboard de Jeedom
Le plugin ne s'affiche pas sur le Dashboard de Jeedom mais dans un panel. Il faut se rendre dans l'onglet Accueil->Suivi Conso

#### Le Panel ne s affiche pas dans L'onglet Accueil
Il faut activer l'affichage dans la configuration du plugin (Plugin -> Gestion des plugins -> suivi Conso -> Afficher le panel desktop)

#### Le plugin ne passe pas de HP a HC
Si vous passez par le plugin teleinfo, il faut verifier que la commande PTEC soit de type Autre puis relancer le Deamon Téléinfo

#### Table 'jeedom.conso_tmp' doesn't exist
Erreur sur conso::StartDeamon() : [MySQL] Error code : 42S02 (1146). Table 'jeedom.conso_tmp' doesn't exist

Exécuter la requête MySql dans la base de données pour recréer la table

```sql
CREATE TABLE `conso_tmp` (
  `id_ecq` int(11) NOT NULL,
  `hp` bigint(20) DEFAULT NULL,
  `hc` bigint(20) DEFAULT NULL,
  `ptec` varchar(255) DEFAULT NULL,
  `lastvalue` bigint(20) DEFAULT NULL,
  `variation` bigint(20) DEFAULT NULL,
  `date_upd` datetime DEFAULT NULL,
  `tmp_value` float DEFAULT NULL,
  PRIMARY KEY (`id_ecq`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
```
