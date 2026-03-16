# Réplication MariaDB Master-Master

## Présentation du projet

Dans le cadre de ma formation BTS SIO option SISR, j'ai mis en place une réplication bidirectionnelle entre deux serveurs MariaDB afin d'assurer la haute disponibilité des données d'une application web.

L'objectif de ce projet est de garantir la continuité de service et la synchronisation des bases de données entre deux nœuds.

Ce type d'architecture est utilisé dans les environnements professionnels pour améliorer la résilience des services critiques.

---

## Architecture

L'infrastructure repose sur deux serveurs Debian hébergeant MariaDB.

Serveur 1  
IP : 172.18.155.X

Serveur 2  
IP : 172.18.155.X

Les deux serveurs sont configurés en réplication maître ↔ maître afin que chaque serveur puisse répliquer les modifications vers l'autre.

---

## Technologies utilisées

- Debian Linux
- MariaDB
- Réplication MySQL/MariaDB
- Binlog
- Application web

---

## Fonctionnement

Chaque serveur agit à la fois comme maître et comme esclave.

Les transactions effectuées sur un serveur sont automatiquement répliquées vers l'autre serveur grâce aux journaux binaires (binlog).

Cette configuration permet :

- la synchronisation automatique des données
- la tolérance aux pannes
- la continuité de service

---

## Tests réalisés

Plusieurs tests ont été réalisés pour vérifier le bon fonctionnement de la réplication :

- création de données dans la base
- vérification de la synchronisation entre les serveurs
- arrêt d'un nœud pour tester la continuité de service

Les résultats confirment que les données restent accessibles et synchronisées entre les deux serveurs.

---

## Compétences mises en œuvre

- Administration Linux
- Configuration MariaDB
- Mise en place d'une réplication de bases de données
- Tests de haute disponibilité
- Diagnostic et vérification de la synchronisation
