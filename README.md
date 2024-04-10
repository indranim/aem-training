### AEM Training TP1
## Architecture

https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/underlying-technology/introduction-architecture
##### Granite
AEM three major layers and three core technology architecture diagram

![AEM Architecture](https://github.com/indranim/aem-training/blob/tp1/AEM_Arch.jpg)


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

https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/underlying-technology/introduction-author-publish

Dispatcher
---------------
To optimize the performance of visitors to your website, the dispatcher implements load balancing and caching.

Adobe Experience Manager Authoring Documentation

https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/underlying-technology/introduction-dispatcher

####  AEM Core Concepts
   + Author instance
     Typically, for security, governance, and other reasons, a production site will divide instances of AEM into Author and Publish instances. For more information on deployment architecture (including Author/Publish instances), see documentation about AEM Instances.
	
  + Publish instance
	For security, governance, and other reasons, a production site will typically divide instances of AEM into Author and Publish instances. For more information on deployment architecture (including Author/Publish instances), see documentation about AEM Instances.
	
  + Component
	In AEM, a Component is an object type, instances of which can generally be created by dragging and dropping them from, say, the Sidekick. So for example, out-of-the-box components that ship with AEM include the Text, Title, Tag Cloud, Carousel, Image, and List components, all available from the Sidekick at runtime.
	
  + Digital assets
	In AEM, Digital Assets are (typically) images and rich media files. For further information, see Working with Digital Assets in DAM.
	
  + Template
	In AEM, a Template specifies a particular type of page. It defines the structure of a page (while also typically specifying a thumbnail image, and various properties). For example, you may have separate templates for product pages, sitemaps, and contact information.
	
      + Workflow
	The AEM Workflow system allows for creation of automated processes involving pages or assets.
  
  + Dispatcher
	The Dispatcher is both a caching and load-balancing tool, as well as providing certain security safeguards.
	
  + JCR, Java Content Repository
	The Java Content Repository specification (JSR-283) provides both an abstract data model and an Application Programming Interface for realizing a massively scalable NoSQL data repository that combines features of a file system and an object database. While you do not need to understand JSR-283 in exhaustive detail, you should take time to familiarize yourself with the basic capabilities of JCR and the data model underlying it, because JCR is what makes possible the "everything is content" philosophy of AEM.
	
	In essence, JCR is a system of nodes and properties, in which nodes can inherit from other nodes and all content is stored as property values. Note that in addition to ordinary inheritance, JCR allows for a concept of "mixin" nodes, which enables modelling of multiple inheritance.
	
	JCR has a number of predefined node types and property types, but in general the typing system is quite flexible, and (indeed) one of the strengths of JCR is that it allows structured as well as unstructured content to be stored/managed with equal ease. That is, JCR can accommodate highly structured data, but it can also accommodate arbitrary dynamic data structures without schema constraints.
	
	The JavaDoc for JCR's Java API is here.
	
	Before attempting to read the JavaDoc or the JCR spec itself, you might want to look at this high-level explanation of JCR as implemented by Adobe Experience Services.

	
  + OSGi
	OSGi is the services-based runtime technology that provides the basis for modularized Java development in AEM. It is a framework that provides not only a highly dynamic (and secure) classloading and execution environment for code resources (known as bundles), but also full control over the visibility and lifecycle of the various services exposed by bundles. A service registry provides a cooperation model for bundles that takes lifecycle dynamics (and version requirements) into account. OSGi solves many of the problems that application servers were intended to solve, but does so in a lightweight, highly dynamic way, making it possible, for example, to hot-deploy services (making the new code immediately available without restarting the server).	
	
  + Quickstart
	Unlike many other programs, you install AEM by using a single "Quickstart" self-extracting JAR file. When you double-click the JAR file for the first time, everything you need is automatically installed. The quickstart JAR includes all files required for the CRX repository (including administrative facilities), virtual repository services, index and search services, workflow services, security, and a Web server, plus the CQ Servlet Engine (CQSE) and all AEM services. There are no other files to install: the Quickstart is self-contained.
	
    The first time you start the Quickstart, it creates an entire JCR-compliant repository in the background, which can take several minutes. After this initial startup, subsequent startups are much quicker as the repository infrastructure has already been laid down.
	
    Many startup options (such as the active port number and whether the AEM instance in question should be a Publish instance versus an Author instance; and much more) can be controlled by appropriately renaming the Quickstart file. To see a list of options in this regard, run the JAR with "-help" on the command line:
	**java -jar <quickstartfilename>.jar –help**

Good Learning
