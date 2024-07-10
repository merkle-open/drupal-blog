---
title: Installation of GraphQL
date: 2024-04-19
author: Miloš Rajčić
tags: ["drupal", "graphql", "acquia", "drupal-planet"]
---

If you wish to start a new Drupal project with GraphQL or add it to the existing one I would wholeheartedly recommend using Acquia CMS Starter Kit that is specifically designed for the headless approach.
There are fewer options in this CMS (e.g. no theming options)  so that you can dedicate as much time as possible to the headless option. Acquia CMS is intended to preconfigure Drupal to serve structured, RESTful content to mobile apps, smart displays, frontend driven websites, etc.

Acquia has this amazing guide on how to install said CMS, but don’t you worry I will give you a speed ride here.

So, to install a new project via composer you would use the following command:

`composer create-project acquia/drupal-recommended-project my_project`

The headless starter kit is available in the project by default. If you wish to add it to the existing project via composer, you would be using the following command:

`composer require acquia/acquia-cms-starterkit`

Once that is done you need to run the following command:

`./vendor/bin/acms acms:install`

When you start this command you will be asked to choose what you wish to install and to answer some questions so that the CMS can be configured to your needs right away.
You would of course choose **acquia_cms_headless** and after that you can choose whether you want demo content, all the content types, if you wish to install next.js (a flexible React framework), Google Maps API Key and database information (name, driver, username, password, host and port).

Your project needs to be setup so that the Drupal core, modules and so on are located in the `docroot` folder.  If you have any other setup (e.g. Drupal in `web`) the install process won’t work!

When the installation is done you will see the following screen.

{{< figure link="images/acquia_cms_headless_backend.png" caption="Acquia CMS Headless Backend" alt="Acquia CMS Headless Backend" >}}

To reach the GraphQL part follow this path: `System administration > Configuration > Web services > GraphQL` (/admin/config/graphql)

There you need to create a new server (for example movies, books, articles, etc), choose your schema (in [the next blog post](/drupal-graphql-how-to-create-a-new-schema) we will see how to create a custom schema, but for the moment stick with the default one).

Once you are done with that, click on **Save** and then return to the just created server by using the **Edit** option.

There you will find the Explorer option. This is your best friend when it comes to working with GraphQL. Here you can write queries and test your schema.

{{< figure link="images/graphql_explorer.png" caption="GraphQL explorer in Drupal" alt="GraphQL explorer in Drupal" >}}

Now that you know how to install and use Acquia CMS Starter Kit the next part is how to retrieve content using GraphQL. In the following blog post I will talk more about that, so stay tuned!
