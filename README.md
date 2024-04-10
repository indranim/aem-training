### AEM Training TP1
## Architecture

https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/underlying-technology/introduction-architecture
##### Granite
AEM three major layers and three core technology architecture diagram

![在这里插入图片描述](https://github.com/indranim/aem-training/blob/tp1/AEM_Arch.jpg)


AEM is composed of a series of Open Source Frameworks such as:

Apache Sling
A framework for RESTful web applications based on an extensible content tree.
Sling maps HTTP request URLs to content resources based on the path, extension, and selectors of the request.
 - Principles of a RESTful Web architecture include:
 - Resource-oriented: every piece of information such as a label, news item, product description, file, or image, for example, is a resource ("everything is content").
 - Resources are addressable and accessible via REST through the HTTP protocol. Each resource has a specific URI.
 - REST is a standardized protocol; one simply uses provided methods like GET, POST, PUT, or DELETE to interact with content.
 - Representation-oriented: an object is referenced by a unique URI but may have different available representation formats. For example, an AJAX request demands JSON, a Java application requests XML, a web browser wants HTML. To address this, different representation and rendering services can be created for each type of resource.
 - Stateless communication: REST itself is stateless; it does not use cookies, and clients must re-authenticate with each request.
   
https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/underlying-technology/introduction-sling
https://sling.apache.org/documentation/tutorials-how-tos.html
https://sling.apache.org/docs/ApacheConEU08_JCR_Meetup_Sling_Architecture.pdf
Apache Sling :: Servlet Resolution
			 [https://sling.apache.org/old-stuff/servlet-resolution.html](https://sling.apache.org/old-stuff/servlet-resolution.html)
			Apache Sling :: URL decomposition
			 [http://sling.apache.org/documentation/the-sling-engine/url-decomposition.html](http://sling.apache.org/documentation/the-sling-engine/url-decomposition.html)
			Apache Sling :: HTL Scripting
			 [https://sling.apache.org/documentation/bundles/scripting/scripting-htl.html](https://sling.apache.org/documentation/bundles/scripting/scripting-htl.html)
			Apache Sling :: Sling Models
			 [https://sling.apache.org/documentation/bundles/models.html#specifying-an-alternate-adapter-class-     since-110](https://sling.apache.org/documentation/bundles/models.html#specifying-an-alternate-adapter-class-%20%20%20%20%20since-110)
			bibliography:
			 [Continuous Delivery of Apache Sling Applications](https://github.com/tobywang11030/mangoCMS/blob/master/Continuous%20Delivery%20of%20Apache%20Sling%20Applications.pdf)
			 [Server-side OSGi with Apache Sling](https://github.com/tobywang11030/mangoCMS/blob/master/Server-side%20OSGi%20with%20Apache%20Sling.pdf)

JCR 
-----
- Content management: Java Content Repository, also known as JSR 283 (formerly known as JSR 170).
- Java Content Repository is a semi-structured data storage space in the form of a tree of nodes. Each item is either a node or a property. A property stores information (name and associated value), while a node structures the content.
- Java Content Repository Presentation 
https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/underlying-technology/introduction-jcr

Apache Jackrabbit Oak 
-----------------------
As an implementation of JCR. Previous versions, up to version 5.6, used Adobe CRX. Oak and CRX provide an API for easier interaction with JCR.
Java Content Repository with Jackrabbit Presentation
https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/introduction/platform

https://jackrabbit.apache.org/oak/docs/

OSGI
----
- A Java platform for installing, starting, and modifying code components, called "bundles," on the fly, i.e., without restarting the server.
- An OSGI solution brings numerous benefits:
- Code becomes easier to write and test due to componentization.
- Component reuse is improved (ease of use).
- Bundle deployments are straightforward (standardized Zip files to install via an administration console).
- Bugs are detected earlier.
- The OSGI engine allows you to see in real-time which components are active and visualize dependencies between them.

https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/underlying-technology/introduction-osgi
**OSGI Tutorial** --https://www.vogella.com/tutorials/OSGi/article.html

Apache Felix
--------------
An implementation of the OSGI platform providing an administration console and an API for easily creating OSGI bundles and interacting with deployed code (concepts of servlets, services, etc.).
[Adobe Meetup AEM Architecture Presentation](https://felix.apache.org/documentation/tutorials-examples-and-presentations/apache-felix-osgi-tutorial.html)

Environments
============
Author
------------
These interact to enable you to make the content available on your website so that your visitors can read it.

The authoring environment provides mechanisms for creating, updating, and revising this content before publishing it:

An author creates and reviews the content (which can be of various types, such as pages, items, posts, etc.) that will be published on your website at some point.

Publish
------------
For the publishing environment, you design all aspects of the interface made available to your users.

Dispatcher
---------------
To optimize the performance of visitors to your website, the dispatcher implements load balancing and caching.

Adobe Experience Manager Authoring Documentation

https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/underlying-technology/introduction-author-publish

Good Learning
