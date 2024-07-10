---
title: How to create a new schema in GraphQL
date: 2024-05-10
author: Miloš Rajčić
tags: ["drupal", "graphql", "drupal-planet"]
---

In order to access data from your own content types you need to create an access point which is based on a schema. A schema defines a hierarchy of types with fields that are populated from your backend data stores.
The schema also specifies exactly which queries and mutations are available for clients to execute.

The first step that is recommended, is to create a custom module in Drupal like you would normally do.
After that you need to copy the examples files from the example module that comes with GraphQL. The most 3 files that you need are:
* `yourModuleName.graphqls`
* `yourModuleName_extension.base.graphqls`
* `yourModuleName_extensio.extension.graphqls`


The file `yourModuleName.graphqls` (example: movie.graphqls) represents your schema where you need to define your queries for your Drupal content type "Movie".
One example of a query would be:

```
# Query definition
schema {
    query: Query
}

# Connection to schema Movie
type Query {
    movie(id: Int!): Movie
        movies(
            offset: Int = 0
            limit: Int = 10
    ): MovieConnection!
}

# Movie query
type Movie {
    id: Int!
    title: String!
    body: String!
}
```

In the first part we define that it’s a Query, which means that you’re using it to get the data. With Mutations we insert the data into the database, but that’s a story for another blog post.

In the next step you make a connection to a certain schema. In this case to "Movie".

And then you create the query itself by defining the data you want to retrieve.
You need to specify data types and when you put the exclamation point on the end that means that you expect only that data type and any other will throw an error.

This is now your first simple schema.

Now what you need are data producers. That is in a nutshell a php code in which you retrieve the data from the database and connect them with your fields in the schema.
Thanks to this connection, users can retrieve the data. I will speak more about the data producers in the next blog post.
