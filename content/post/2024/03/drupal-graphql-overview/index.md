---
title: Drupal GraphQL Overview
date: 2024-03-25
author: Miloš Rajčić
tags: ["drupal", "drupal-planet", "graphql"]
---

[GraphQL](https://graphql.org/) is an open-source language for APIs that allows us to query and manipulate data. GraphQL uses one exported endpoint to retrieve structured data, just the way a client asked for. Since GraphQL has the ability to get the data from separate sources and combine them in a single response, we can conclude that GraphQL is very versitile and isn’t tide to any specific storage engine or database.

GraphQL had its beginnings in 2012, but the first release was in 2015. Afterwards in 2018 Linux Foundation established GraphQL Foundation took over further development and standardization. Even though GraphQL was developed by Facebook, many public APIs have adopted it as a primary way of accessing them. Some of these public APIs include Shopify, Yelp, Github, Google Directions API and of course Facebook, as well as many others.

### Key aspects of GraphQL

**Declarative Data Fetching** - 
Clients can avoid over-fetching or under-fetching because GraphQL allows them to request only the data that they need and in the order they need it.

**Hierarchical Structure** - 
GraphQL makes complex queries easy to understand and compose, because of the hierarchical structure in which the data is requested.

**Strongly Typed Schema** - 
GraphQL APIs are based upon a schema in which all the types of data are specified and their relationships as well. Thanks to this feature we have a lot of powerful tools and validation options.

**Single Endpoint** - 
Traditional REST APIs often have multiple endpoints for different resources. However, GraphQL usually uses only one endpoint because we can request as much or as little data as we want.

**Real-Time Updates** - 
Because of the subscriptions features clients can receive real-time updates when the data is changed on the server.

**Introspection** - 
Introspection feature allows clients to query the schema in order to discover which data types, relationships and fields are available.

**Backend Agnostic** - 
Introspection feature allows clients to query the schema in order to discover which data types, relationships and fields are available.	Being Backend Agnostic means that we can use GraphQL with any programming language or data storage system.

In a nutshell, GraphQL is a powerful, efficient and flexible way to access the APIs which allows clients to retrieve only the data that they need and in the way they need it. Because of this GraphQL has become very popular in building mobile and web apps.

## The difference between JSON:API & GraphQL

[JSON:API](https://jsonapi.org/) and GraphQL are both popular technologies used for building APIs in web and mobile development, but they have different approaches, features and characteristics. Here's a comparison of the two:

**Data Retrieval and Querying**
| JSON:API | GraphQL |
| --- | --- |
| When talking about JSON:APIs the response structure is defined by the server and the client gets all the data in a JSON format, wether needed or not. | GraphQL allows clients to request only the data that they need and in the order they need it. Thanks to this clients also have the ability to join multiple resources in a single response. |

**Response Structure**
| JSON:API | GraphQL |
| --- | --- |
| Response structure is defined by the JSON:API specification. Since the structure is following the same pattern, it’s easy for the clients to get the data.  | GraphQL response is typically a JSON object that has the same structure as the query that client requested.  |

**Schema Definition**
| JSON:API | GraphQL |
| --- | --- |
| Server defines the endpoints and the structure of the data being returned by said endpoints. | Server defines a schema that contains all the data types and the relationships between them. Clients can query the schema to see what is available and retrieve only the data that they need. |

**Versioning**
| JSON:API | GraphQL |
| --- | --- |
| Whenever the data is changed a new version of the API is created and the client decides which version should be used. | In GraphQL changes to the schema can be made without the client noticing anything. Even though the data has changed the client can still request the exact data as before. |

**Caching**
| JSON:API | GraphQL |
| --- | --- |
| Caching in JSON is usually achieved using HTTP caching headers (e.g., Cache-Control, ETag). Clients can cache responses based on these headers. | In GraphQL tools such as persisted queries and response caching can help improve the caching process. Caching is complex when we are dealing with queries since their shape and structure can vary. |

Simply put, both JSON:API and GraphQL are powerful tools for building APIs with their own pros and cons. The choice between the two depends on the preferences and requirements of a project we are working on.

## Drupal & GraphQL

When it comes to using GraphQL with Drupal, Drupal has embraced GraphQL as a way to expose its content and capabilities through a GraphQL API. The integration of GraphQL in Drupal allows developers to query Drupal's content and data using GraphQL syntax, providing more flexibility and efficiency compared to traditional RESTful approaches.

The Drupal GraphQL module provides an integration layer between Drupal and GraphQL. It allows Drupal developers to expose Drupal entities (such as nodes, users, and taxonomy terms) as GraphQL types, fields, and mutations.
With GraphQL in Drupal, clients can request specific data structures tailored to their needs, reducing over-fetching and under-fetching of data.

GraphQL APIs generated by Drupal come with built-in documentation, which allows developers to explore available types, fields, and relationships interactively. This makes it easier to understand and work with the API.

Drupal's GraphQL implementation supports real-time updates through subscriptions. Clients can subscribe to change in Drupal entities and receive updates in real-time, making it suitable for building interactive applications.

The integration of GraphQL with Drupal provides developers with a modern and efficient way to interact with Drupal's content and data, offering more flexibility and better performance compared to traditional REST APIs. It empowers developers to build rich, interactive web applications while leveraging Drupal's robust content management capabilities.

In upcoming blog installments, I will guide you through the seamless integration of GraphQL with Drupal. With the version 4 of GraphQL, developers are faced with a wave of changes, prompting the need for custom code to unlock its full potential. Together, we will navigate through comprehensive examples, demystifying the process of setting up GraphQL within your Drupal project, creating schemas to streamline data organization, and executing queries to fetch precisely the information you require. Furthermore, we will delve into advanced concepts such as mutations for data manipulation, subscriptions for real-time updates, and indispensable best practices to optimize your GraphQL API.

Stay tuned for a comprehensive journey into harnessing the power of GraphQL alongside Drupal to create dynamic and efficient web applications!