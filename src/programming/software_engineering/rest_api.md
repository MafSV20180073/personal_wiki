# REST API

## Naming conventions

<br>

![Restful Endpoint](images/restful_endpoint.png "a title")


1. Use nouns to represent resources, not verbs;
2. Use pluralized nouns for resources;
3. Use hyphens (`-`) to improve the readability of URIs;
4. Use forward slashes (`/`) for hierarchy but not trailing forward slash;
5. Avoid using file extensions;
6. Version your APIs;
7. Use query component to filter URI collection (parameters should be passed after the `?`);
8. RESTful error handling and status response messages (the API should provide meaningful error messages in a common prescribed format).

## Why use REST APIs?

- REST uses all of the standard http protocal methods (GET, POST, PUT, ...) together with URIs for added flexibility;
- REST separates operations between the client and the server;
- REST is simpler than SOAP;
- REST is optimized for the web, and since its main data format is JSON, it is basically compatible with all internet browsers;
- REST allows many different data formats (it supports plain text, HTML, XML, JSON, ZIP, PDF, CSV, ...);
- REST features excellent performance and scability;
- REST is rapidly evolving and has been already implemented in multiple languages.

<br><b>Additional notes:</b>

- The URIs (Uniform Resource Identifiers) are named with nouns to specify the resource instead of using verbs;
- The URIs should not indicate any CRUD (create, read, update, delete);
- Avoid verb-noun combinations;
- Use plural when possible unless they are singleton resources;
- Avoid using underscores in the URIs;
- Forward slashes are used to show the hierarchy between individual resources and collections;
- Enable sorting, filtering, and pagination in the resource collection API and give the input parameters as query parameters to meet this requirement;
- The key abstraction of information in REST is a resource (any information that can be named can be a resource);
- - In REST, the primary data representation is called a <i>resource</i>;
- A resource can be a singleton or a collection;
- A resource may contain sub-collection resources;
- A resource is a conceptual mapping to a set of entities, not the entity that corresponds to the mapping at any particular point in time.
  
<br>

<br>

**Main sources:**

- https://medium.com/@nadinCodeHat/rest-api-naming-conventions-and-best-practices-1c4e781eb6a5
- https://restfulapi.net/resource-naming/
- https://avaldes.com/best-practices-for-restful-api-design/
