---
title: introduction
---
- **Contexte général** 
	![[Pasted image 20240212182801.png]]
- **Jakarta**
	![[Pasted image 20240212182818.png]]
	- 1. **Plateforme Jakarta EE** : C'est une ==***plateforme*** ***logicielle***== qui fournit un ensemble de spécifications pour le développement d'applications Java d'entreprise. Ces spécifications incluent des fonctionnalités telles que ***==l'injection de dépendance==*** (CDI & DI), la gestion des WebSocket, des services web (SOAP ou REST), ainsi que le traitement et la liaison de données JSON.
    
	- **Composants d'Applications Jakarta EE** : Ces composants sont les éléments de base qui constituent une application Jakarta EE. Le texte mentionne quatre types de composants :
    
	    - a. **Application Client Container** : Il s'agit de composants qui sont exécutés sur un poste de travail (desktop). Ce sont généralement des interfaces utilisateur graphiques (GUI).
    
	    - b. **Web Container** : Ces composants répondent aux requêtes HTTP des clients Web. Les servlets, les filtres et les écouteurs d'événements web sont des exemples de composants qui s'exécutent dans des conteneurs web. Ils sont utilisés pour générer du contenu HTML, JSON ou XML dynamiquement.
    
	    - c. **Entreprise Beans Container** : C'est un environnement d'exécution pour les composants qui nécessitent la gestion des transactions. Les composants exécutés dans ce conteneur sont souvent utilisés pour gérer la logique métier de l'application.
    
	- **Objectif du Cours** : Le cours se concentre sur l'utilisation des conteneurs web pour répondre aux requêtes HTTP des clients, ce qui signifie que l'accent sera mis sur la création d'applications web utilisant des technologies Jakarta EE.

	- En résumé, Jakarta EE est une plateforme pour le développement d'applications d'entreprise en Java, et les composants d'application Jakarta EE incluent des conteneurs pour les applications clientes, les applications web et les beans d'entreprise. Ce cours se concentrera sur l'utilisation des conteneurs web pour répondre aux requêtes HTTP des clients.
- **Jakarta Restful Web Service**
	- **AX-RS** : C'est l'acronyme de Jakarta RESTful Web Services, anciennement connu sous le nom de Java API for RESTful Web Services. C'est une spécification de l'API Jakarta EE qui permet de créer des services web selon l'architecture REST (Representational State Transfer).

	- **Annotations JAX-RS** : JAX-RS fournit un ensemble d'annotations qui facilitent le développement de services web RESTful en Java. Ces annotations sont utilisées pour mapper des ressources web à des POJOs (Plain Old Java Objects) et pour extraire des informations à partir des requêtes. Voici quelques exemples d'annotations importantes :
		- `@Path`: Utilisée pour spécifier le chemin d'accès relatif à la ressource.
		- `@GET`: Utilisée pour spécifier une méthode HTTP GET.
		- `@Produces`: Utilisée pour spécifier le type de contenu produit par la ressource.
		- `@PathParam`: Utilisée pour extraire des valeurs des parties variables de l'URI.
		- `@QueryParam`: Utilisée pour extraire des valeurs des paramètres de requête.

	- **POJO** : C'est l'acronyme de Plain Old Java Object. Un POJO est simplement un objet Java ordinaire qui n'implémente pas une interface prédéfinie ou n'étend pas une classe prédéfinie de la plateforme Java.

	- **JavaBean** : C'est un type spécifique de POJO qui suit certaines conventions, telles que l'implémentation de l'interface Serializable, la présence d'un constructeur sans argument et l'utilisation de méthodes getters et setters pour accéder et modifier les propriétés de l'objet.

	- **Implémentations de JAX-RS** : En plus de Jersey, qui est l'implémentation de référence de JAX-RS fournie par Sun et intégrée à GlassFish, il existe d'autres implémentations telles que Apache CXF et RESTEasy.

	- **Documentation Jersey** : Pour développer des APIs RESTful en Java avec Jersey, la meilleure documentation est le guide de l'utilisateur de Jersey 3.1.5 disponible sur le site officiel de Jersey.

	En résumé, JAX-RS est une spécification de Jakarta EE qui facilite le développement de services web RESTful en Java en fournissant des annotations pour mapper des ressources et extraire des informations des requêtes, tandis que Jersey est l'une des implémentations les plus populaires de cette spécification.
	
- **technologie pour les web services**
	ce que nous allons utiliser en cours :
	- Eclipse Jersey** (anciennement **Glassfish Jersey**) pour l’aspect annotations et la gestion des ressources, pour l’injection de dépendances ;
	- Le serveur http **Grizzly** qui est construit sur **Java NIO** (Non-blocking IO, ou New IO permettant d’avoir plusieurs traitements en parallèle au sein d’un thread), qui offre un http container qui exécute des applications JAX-RS ;
	- **Jackson** pour la gestion du **JSON** ;
	- **Java JWT** pour la gestion de l’authentification et de l’autorisation via des token ;
	- **jBCrypt** pour la gestion des passwords (hashing).
