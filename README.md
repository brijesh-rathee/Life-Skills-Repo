# REST Architecture: A Technical Overview

## Introduction

Representational State Transfer (REST) is an architectural style that prescribes a set of constraints for designing web services that scale. Developed by Roy Fielding in his 2000 doctoral dissertation, REST has since become the de facto model for designing APIs on the web.

## Key Principles of REST

REST is based on six fundamental architectural constraints:

### 1. Statelessness
Each client request to a server must include all the information needed to interpret and process the request. The server holds nothing regarding the client's session between requests.

Reference: https://www.ics.uci.edu/~fielding/pubs/dissertation/rest_arch_style.htm

### 2. Client-Server Architecture
The REST architecture makes the client and server separate. Clients and servers can be written and released separately because of this separation.

### 3. Cacheability
The responses should clearly specify if they are cacheable. If cacheable, responses can be reused for the same requests to optimize performance and limit server load.

### 4. Uniform Interface
A uniform interface keeps the architecture simple and decoupled. It consists of:
- Resource identification by URIs
- Resource manipulation by representations
- Self-descriptive messages
- Hypermedia as the engine of application state (HATEOAS)

### 5. Layered System
A REST system may consist of more than one layer, with each layer only knowing the next immediate layer it is communicating with.

### 6. Code on Demand (Optional)
Servers can add client capabilities by delivering executable code, like JavaScript.

## HTTP Methods in REST

RESTful APIs use standard HTTP methods to manipulate resources:

| Method  | Description                      |
|---------|----------------------------------|
| GET     | Retrieve a resource              |
| POST    | Make a new resource            |
| PUT     | Replace or update a resource     |
| PATCH   | Update a resource partially      |
| DELETE | Delete a resource              |

Reference: https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods

## RESTful URL Design

RESTful APIs are based on resources. Resource URIs are nouns, not verbs. Actions are executed using HTTP methods.

Example URL structures:

GET /users - Get all users
GET /users/{id} - Get a user by ID
POST /users - Create a new user
PUT /users/{id} - Update a user
DELETE /users/{id} - Delete a user

Reference: https://restfulapi.net/resource-naming/

## Benefits of REST

- Simple and consistent interface
- Stateless interactions enhance scalability
- Takes advantage of standard HTTP features (e.g., caching, status codes)
- Language-independent
- Simple integration with existing web infrastructure

## Restraints of REST

- Statelessness can lead to redundant information exchange
- Versioning or type safety is not built-in
- Limited flexibility in querying compared to newer options like GraphQL
- Complex query handling might be less efficient

## REST vs Other API Architectures

| Feature         | REST            | SOAP           | GraphQL         |
|-----------------|------------------|----------------|-----------------|
| Protocol        | HTTP             | HTTP, SMTP     | HTTP            |
| Data Format     | JSON, XML        | XML            | JSON            |
| Flexibility     | Medium           | Low            | High            |
| Caching         | Fully supported  | Limited        | Partially       |
| Learning Curve | Low              | High           | Medium          |

Reference: https://www.ibm.com/cloud/blog/rest-vs-soap-vs-graphql

## Best Practices for Designing REST APIs

- Use plural nouns to name resources (`/books`, not `/book`)
- Consistently use HTTP status codes (e.g., 200 OK, 404 Not Found)
- Version your APIs (`/v1/users`)
- Proper error handling
- Secure your APIs (e.g., OAuth2, HTTPS)

## Conclusion

REST is a robust, versatile, and scalable architecture for web API development. Its commitment to web standards and stateless nature ensure that it is the best approach for developing distributed systems and services.

## References

1. Fielding, Roy T. "Architectural Styles and the Design of Network-based Software Architectures." https://www.ics.uci.edu/~fielding/pubs/dissertation/rest_arch_style.htm
2. REST API Tutorial. https://restfulapi.net
3. Mozilla Developer Network - HTTP Methods. https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods
4. IBM - REST vs SOAP vs GraphQL. https://www.ibm.com/cloud/blog/rest-vs-soap-vs-graphql
