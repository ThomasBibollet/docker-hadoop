Nom du projet : Cloudera - Hadoop avec Docker-Compose

Description :
Sur Docker, on a plusieurs conteneurs qui permettent de créer un cluster Hadoop Cloudera

L'intérêt est de réunir nos différents conteneurs pour les assembler
Docker-Compose va créer un seul réseau pour notre application et permettre de relier les conteneurs
Il suffit de régler les ports pour lier les conteneurs ensemble pour avoir notre application

Schéma de l'architecture:
-2 datanodes
-1 edgenode (noeud maitre)
-1 namenode
-1 yarnmaster

Explication des conteneurs:

Le datanode permet de traiter les données de façon distribuée, sur Hadoop les données sont stockées sur des blocs de 128 mégaoctets.
L'edgenode nous permet de communiquer avec le cluster. Il nous sert de passerelle pour communiquer avec les autres noeuds.
Le namenode permet de gérer le système de fichiers et les datanodes.
Le yarnmaster permet de distribuer les tâches et de gérer les ressources (YARN).

Liens :
https://hub.docker.com/r/loicmathieu/cloudera-cdh-edgenode
https://hub.docker.com/r/loicmathieu/cloudera-cdh-datanode
https://hub.docker.com/r/loicmathieu/cloudera-cdh-namenode
https://hub.docker.com/r/loicmathieu/cloudera-cdh-yarnmaster