_Project Name_: 

**Cloudera - Hadoop with Docker-Compose**

_Description_:

On Docker, we have several containers that allow us to create a Cloudera Hadoop cluster

The interest is to gather our different containers to assemble them
Docker-Compose will create a single network for our application and allow us to connect the containers
We just need to set the ports to link the containers together to have our application

Architecture diagram_:

-2 datanodes

-1 edgenode (master node)

-1 namenode

-1 yarnmaster

_Explanation of containers_:

The datanode allows us to process data in a distributed way, on Hadoop data is stored on 128 megabyte blocks.
The edgenode allows us to communicate with the cluster. It serves as a gateway to communicate with other nodes.
The namenode allows us to manage the file system and the datanodes.
The yarnmaster allows us to distribute tasks and manage resources (YARN).

How it works:
1) Download the images

docker pull loicmathieu/cloudera-cdh-namenode

docker pull loicmathieu/cloudera-cdh-datanode

docker pull loicmathieu/cloudera-cdh-edgenode

docker pull loicmathieu/cloudera-cdh-yarnmaster

2) Launch the application

docker-compose up

3) For Azure :

docker context use contextacihadoop

4) In case of a network error :

net stop hns

_Links_ :

https://hub.docker.com/r/loicmathieu/cloudera-cdh-edgenode

https://hub.docker.com/r/loicmathieu/cloudera-cdh-datanode

https://hub.docker.com/r/loicmathieu/cloudera-cdh-namenode

https://hub.docker.com/r/loicmathieu/cloudera-cdh-yarnmaster
