## What is API
APIs (Application Programming Interface) are sets of definitions and protocols that allow software components to talk and interact with each other using a simple set of commands. Acting as messengers, APIs deliver one application’s request to another and return a response in real time.

APIs are used to make requests to a server and return response to the application, either with the required data or an error message. However, the server needs to handle situations like too many requests at a time. 

## API key
An API key is an unique identifier (a string of letters and numbers) that is used to either grant or deny access to service based on clinet's access permission and track numnber of request made.

## Usages
- Data sharing: service from third party e.g. travel app compiling flight schedules and bookings
- App integrations: two digital applicaions work together e.g. an android app inegrating google services
- Embedded content: embedd twitter or instagram posts
- Internal systems: communication between smaller components of a business

## REST APIs
REST APIs conform to the constraints of a software architectural style called “Representational State Transfer” that make the APIs relatively easy to use and discover. REST makes data and functionality available as resources, which are represented by unique URLs. 

### Key terms
- Client: who is using the API to make the request
- Resourse: piece of information the API will provide to the client
- Server: that hosts the resourse and provides the API to interact with the client with specific requests and resources without giving them direct access to content stored in its database.

## The Six Rules of REST APIs
- Client-Server Separation
  Under REST architecture, the client and server can only interact in one way: The client sends a request to the server, then the server sends a response back to the client. Servers cannot make requests and clients cannot respond — all interactions are initiated by the client.
- Uniform Interface
  A common protocol, or a way of formatting messages that acts as an intermediary for applications and servers written in different languages and platforms.
- Stateless
  All calls with a REST API must be stateless. This means that every interaction is independent, and each request and response provides all the information required to complete the interaction. The server can optimize memory usage as there's no need to remember past interactions.
- Layered System
  There are typically more servers between a client and server. These servers, or layers, are there to add security, handle and distribute traffic, or assist with a number of other important functions. Requests should still be formatted and processed the same way, regardless of layers that sit between them. It allows seamless updates to server systems
- Cacheable
  REST APIs are created with data caching in mind. When a server sends its response to a client, the response should indicate whether the resource provided can be cached, and for how long.
- Code on Demand (Optional)
The final REST principle is optional. If desired, an API can send computer code to clients in its response. This empowers the client to run the code in its own backend.

As long as an API adheres to this set of rules, it is considered RESTful. 

Read more on https://blog.hubspot.com/website/what-is-rest-api
