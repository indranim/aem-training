AEM Training TP1
Architecture

Apache Sling
Apache Sling is a framework for RESTful web applications based on an extensible content tree. Sling maps HTTP request URLs to content resources based on the path, extension, and request selectors. The principles of a RESTful web architecture are:

Resource-oriented: Every piece of information, such as a label, news item, product description, file, or image, is considered a resource ("everything is content").
Resources are addressable and accessible via HTTP using the REST protocol. Each resource has a specific URI.
REST is a standardized protocol. It simply uses methods like GET, POST, PUT, or DELETE to interact with content.
Representation-oriented: An object is referenced by a unique URI but can have different representation formats available. For example, an AJAX request demands JSON, a Java application requires XML, and a web browser wants HTML. To address this, different representation and rendering services can be created for each type of resource.
Stateless communication: REST itself is stateless, it does not use cookies, and clients must re-authenticate for each request.
JCR
Java Content Repository (JCR) is an API for a standard document repository also known as JSR 283 (formerly known as JSR 170). It is a semi-structured data storage space in the form of a tree of nodes. Each item is either a node or a property. A property stores information (name and associated value), while a node structures the content.

Apache Jackrabbit Oak
Apache Jackrabbit Oak serves as an implementation of JCR. Previous versions, up to version 5.6, used Adobe CRX. Oak and CRX provide an API to interact more easily with JCR.

OSGI
OSGI is a Java platform that allows the installation, starting, and modification of code components, called "bundles," on the fly, without restarting the server. OSGI offers several benefits:

Environments

Author

These interact to enable you to make content available on your website so that your visitors can read it.

The authoring environment provides mechanisms for creating, updating, and revising this content before publishing it:

An author creates and reviews the content (which can be of various types, such as pages, items, posts, etc.) that will be published on your website at some point.

Publish

For the publishing environment, you design all aspects of the interface made available to your users.

Dispatcher

To optimize the performance of visitors to your website, the dispatcher implements load balancing and caching.

Link to Adobe Experience Manager Documentation

Good Learning
