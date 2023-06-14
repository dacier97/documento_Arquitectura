# DOCUMENTO DE DISEÑO TECNICO
Cliente FOOBREX LOGISTICS 

# TABLA DE CONTENIDO

- Diagrama de Componentes
- Diagrama de Clases
- Diagrama Casos de Uso
- Diagrama Entidad Relacion
- Listado Inferfaces
- Diseño de Interfaces


# Diagrama de Componentes
Los diagramas de componentes UML representan las relaciones entre los componentes individuales del sistema mediante una vista de diseño estática. Pueden ilustrar aspectos de modelado lógico y físico.

<img width="auto" src="diagramaComponentes.drawio.svg" />

# Diagrama de Clases

Diagrama de clases
El diagrama de clases es uno de los diagramas incluidos en UML 2.5 clasificado dentro de los diagramas de estructura y, como tal, se utiliza para representar los elementos que componen un sistema de información desde un punto de vista estático.

<img width="auto" src="diagramaClass.drawio.svg" />


# Diagrama Casos de Uso
El diagrama de casos de uso es una forma de diagrama de comportamiento en lenguaje de modelado unificado (UML, del inglés Unified Modelling Language), con la que se representan procesos empresariales, así como sistemas y procesos de programación orientada a objetos.

<img width="auto" src="diagramaUso.drawio.svg" />

# Diagrama Entidad Relacion

Un diagrama entidad-relación, también conocido como modelo entidad relación o ERD, es un tipo de diagrama de flujo que ilustra cómo las "entidades", como personas, objetos o conceptos, se relacionan entre sí dentro de un sistema

<img width="auto" src="diagramaEntidadRelacion.drawio.svg" />

# Listado Inferfaces

* Spring Boot 2.3.5 / Apache Maven 3.6.3.
* Spring Boot Starter Actuator.
* Spring Cloud Stream.
* Spring Cloud Gateway.
* Spring Cloud Starter Consul Discovery.
* Spring Cloud Starter OpenFeign.
* Springdoc OpenApi.
* Spring Boot Starter Security.
* Spring Security OAuth2.
* ElasticSearch - Logstash - Kibana (ELK Stack).
* MongoDB.
* Mongo DB Express (Web-based MongoDB admin interface, written with Node.js and express).
* Consul Server.
* SSO Keycloak Server.
* Hadoop HDFS.
* Apache Nifi.
* Apache Tika Server.
* Rabbit MQ / STOMP protocol.
* Apache Kafka.
* Kafka Rest Proxy

# Diseño de Interfaces

### Rake Tasks

The available tasks are detailed below (rake --task)


| Task | Description |
| ------ | ------ |
| check_deployment_file_task | Check Deployment File |
| check_docker_task | Check Docker and Docker Compose Task |
| cleaning_environment_task | Cleaning Evironment Task |
| deploy | Deploys the Document Search Engine architecture and laun... |
| login | Authenticating with existing credentials |
| start | Start Containers |
| status | Status Containers |
| stop | Stop Containers |
| undeploy | UnDeploy Document Search Engine architecture |


To start the platform make sure you have Ruby installed, go to the root directory of the project and run the `rake deploy` task, this task will carry out a series of preliminary checks, discard images and volumes that are no longer necessary and also proceed to download all the images and the initialization of the containers.


### Containers Ports

In this table you can view the ports assigned to each service to access to the Web tools or something else you can use to monitoring the flow.

| Container | Port |
| ------ | ------ |
| Apache Nifi Dashboard UI | localhost:8080 |
| Hadoop Resource Manager | localhost:8081 |
| Kafka Topics UI | localhost:8082 |
| MongoDB Express | localhost:8083 |
| Kibana | localhost:8084 |
| Keycloak PGAdmin | localhost:8085 |
| Keycloak Admin UI | localhost:8086 |
| Consul Dashboard | localhost:8087 |
| Rabbit MQ - Stomp Dashboard | localhost:8088 |
| Hadoop NameNode Dashboard | localhost:8089 |
| API Gateway SSH  | localhost:2223 |
| SFTP Server | localhost:2222 |

## Some Videos

[![An architectural approach to implement a large-scale document search engine based on Apache Nifi](https://img.youtube.com/vi/-wJElnR3St4/maxresdefault.jpg)](https://youtu.be/-wJElnR3St4)

[![An architectural approach to implement a large-scale document search engine based on Apache Nifi](https://img.youtube.com/vi/9aQTO5J7_K4/maxresdefault.jpg)](https://youtu.be/9aQTO5J7_K4)

[![Microservice architecture to interact with the platform](https://img.youtube.com/vi/FZzMTr_z0Lw/hqdefault.jpg)](https://youtu.be/FZzMTr_z0Lw)



## Some screenshots

As follow, I include some images that help us to understand the performance of each part of system

### ETL Flow based on Apache Nifi

Apache NiFi supports powerful and scalable directed graphs of data routing, transformation, and system mediation logic.

<img width="auto" src="./images/apache_nifi_1.PNG" />
<img width="auto" src="./images/apache_nifi_2.PNG" />
<img width="auto" src="./images/apache_nifi_3.PNG" />
<img width="auto" src="./images/apache_nifi_4.PNG" />
<img width="auto" src="./images/apache_nifi_5.PNG" />
<img width="auto" src="./images/apache_nifi_6.PNG" />
<img width="auto" src="./images/apache_nifi_7.PNG" />

### Events System based on Apache Kafka

Apache Kafka is an open-source distributed event streaming platform used by thousands of companies for high-performance data pipelines, streaming analytics, data integration, and mission-critical applications.

<img width="auto" src="./images/apache_kafka_1.PNG" />
<img width="auto" src="./images/apache_kafka_2.PNG" />

### Apache Hadoop HDFS to store the files that will proccess

The Hadoop Distributed File System (HDFS) is a distributed file system designed to run on commodity hardware. It has many similarities with existing distributed file systems. However, the differences from other distributed file systems are significant. HDFS is highly fault-tolerant and is designed to be deployed on low-cost hardware. HDFS provides high throughput access to application data and is suitable for applications that have large data sets. HDFS relaxes a few POSIX requirements to enable streaming access to file system data. HDFS was originally built as infrastructure for the Apache Nutch web search engine project. HDFS is now an Apache Hadoop subproject.

<img width="auto" src="./images/hdfs_1.PNG" />
<img width="auto" src="./images/hdfs_2.PNG" />
<img width="auto" src="./images/hdfs_3.PNG" />

### MongoDB to store the metadata and content of the files that have been proccessed.

<img width="auto" src="./images/mongodb_1.PNG" />
<img width="auto" src="./images/mongodb_2.PNG" />
<img width="auto" src="./images/mongodb_3.PNG" />
<img width="auto" src="./images/mongodb_4.PNG" />
<img width="auto" src="./images/mongodb_5.PNG" />

### Consul to coordinate microservices architecture. 

<img width="auto" src="./images/consul_1.PNG" />
<img width="auto" src="./images/consul_2.PNG" />
<img width="auto" src="./images/consul_3.PNG" />

### SSO Keycloak Server

<img width="auto" src="./images/keycloak_1.PNG" />
<img width="auto" src="./images/keycloak_2.PNG" />
<img width="auto" src="./images/keycloak_3.PNG" />
<img width="auto" src="./images/keycloak_4.PNG" />
<img width="auto" src="./images/keycloak_5.PNG" />

### The entry point to the architecture.

<img width="auto" src="./images/gateway_1.PNG" />
<img width="auto" src="./images/gateway_2.PNG" />
<img width="auto" src="./images/gateway_3.PNG" />
<img width="auto" src="./images/gateway_4.PNG" />
<img width="auto" src="./images/gateway_5.PNG" />
<img width="auto" src="./images/gateway_6.PNG" />
<img width="auto" src="./images/gateway_7.PNG" />
<img width="auto" src="./images/gateway_8.PNG" />

### ELK Stack

<img width="auto" src="./images/kibana_1.PNG" />
<img width="auto" src="./images/kibana_2.PNG" />
<img width="auto" src="./images/kibana_3.PNG" />
<img width="auto" src="./images/kibana_4.PNG" />
<img width="auto" src="./images/kibana_5.PNG" />
<img width="auto" src="./images/kibana_6.PNG" />
<img width="auto" src="./images/kibana_7.PNG" />

## Visitors Count

<img width="auto" src="https://profile-counter.glitch.me/document_search_engine_architecture/count.svg" />

## Please Share & Star the repository to keep me motivated.
  <a href = "https://github.com/sergio11/document_search_engine_architecture/stargazers">
     <img src = "https://img.shields.io/github/stars/sergio11/document_search_engine_architecture" />
  </a>
  <a href = "https://twitter.com/SergioReact418">
     <img src = "https://img.shields.io/twitter/url?label=follow&style=social&url=https%3A%2F%2Ftwitter.com%2FSergioReact418" />
  </a>

