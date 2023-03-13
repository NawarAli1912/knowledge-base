- sets of protocols, routines, and tools for building software applications. They specify how [[#software components]] should interact with each other, and they can be used to enable communication between different systems, services, and applications.
  </br>
- Web services and web APIs are often used interchangeably and refer to APIs that are accessed over the internet using standard web protocols such as HTTP. They provide a standardized way for applications to exchange data and perform operations, regardless of the underlying technology or programming language used.
  </br>
- REST (Representational State Transfer) is a style of software architecture that uses HTTP and other web standards to create scalable and flexible web services. RESTful APIs use HTTP methods such as GET, POST, PUT, and DELETE to perform CRUD (Create, Read, Update, Delete) operations on resources.
  </br>
- RESTful any service which is built using REST architecture is called RESTful service so RESTful API is an API that were build using REST architecture.
  </br>
- it is worth noting that REST APIs are often used in web services because they are compatible with the HTTP protocol, which is the foundation of the web. Therefore, they are well-suited for exchanging data between web servers and clients.
  </br>
- EX1: 
  if you have a hardware device that needs to be controlled by a software application, you might use an API provided by the device manufacturer to send commands to the device and receive data from it.
  </br>
- EX2:
  Google Maps API: The Google Maps API provides developers with a set of tools for integrating Google Maps into their applications. With this API, developers can add maps and location data to their applications, and customize the appearance and behavior of the maps.

## Interview Questions
- How are REST APIs stateless ?
  each request made by the client to a rest api must contain all necessary that particular http method. 
  </br>
- Explain HTTP methods ?
  GET fetches a resource(s) from the server.
  POST requests for a resource to be created on the server.
  PUT requests for a resource to be updated on the server.
  DELETE request for a resource to be deleted.
  they correspond to the crud operations.
  </br>
- What is a URI ?
  it stands for Uniform resource identifier 
  it identify every resource the rest architecture can be one of two types :
  - urn which identify a resource throw unique and persistent name 
  - url which are typical web address.
  In summary, URI is the umbrella term that encompasses both URL and URN. URLs are a type of URI that provides the location of a resource on the internet, while URNs are a type of URI that provides a persistent identifier for a resource on the internet.
  </br>
-





### software components :
A software component can be a module, a library, a package, or a service, and it can be written in any programming language. Software components are designed to be reusable, meaning that they can be used in multiple applications or systems.