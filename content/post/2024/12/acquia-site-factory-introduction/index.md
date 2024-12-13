---
title: Acquia Site Factory - Introduction
date: 2024-12-10
author: Milovan Krivokapić
tags: ["acquia", "acquia-site-factory", "drupal-planet"]
---
In today's digital landscape, managing multiple websites efficiently is a critical challenge for many organizations. 
Enter Acquia Site Factory, a robust platform designed to streamline the creation, management, and delivery of numerous 
sites from a single, centralized interface. Let's explore how Acquia Site Factory is transforming multisite management.

## What is Acquia Site Factory?
Acquia Site Factory is a comprehensive platform that empowers organizations to manage a portfolio of websites with ease. 
Whether you're overseeing multiple brands, regional sites, or campaign-specific pages, Site Factory provides the tools 
needed to maintain consistency, security, and performance across all digital properties.

## Key Features and Benefits
1. **Multisite Management**: With Acquia Site Factory, you can build, manage, and update multiple sites from one platform. 
This capability is particularly beneficial for organizations with diverse digital needs, allowing for efficient oversight 
and streamlined operations.
2. **Centralized Control**: The platform offers a unified management console where you can monitor and manage all your 
sites. This centralization simplifies governance, ensuring that all sites adhere to the same standards and policies.
3. **Scalability and Flexibility**: Acquia Site Factory supports the creation of sites for different languages and regions, 
making it ideal for global organizations. It also provides role-based access controls and customizable site templates to 
facilitate rapid site creation and management.
4. **High Availability and Security**: Acquia ensures that your sites are always up-to-date and secure with a fully 
managed hosting environment, regular security updates, and 24/7 monitoring. This high level of reliability is crucial for 
maintaining user trust and engagement.
5. **Low-Code Development**: The platform includes pre-built templates and a library of components that enable teams to 
quickly build and deploy sites without extensive coding. This low-code approach accelerates development timelines and reduces costs.

## Why Choose Acquia Site Factory?
Choosing Acquia Site Factory means opting for a solution that prioritizes efficiency, security, and scalability. 
It's designed to help organizations deliver consistent, high-quality digital experiences across all their sites, ensuring 
that each site meets the same high standards.


In a world where digital presence is paramount, Acquia Site Factory stands out as a powerful tool for managing multiple 
websites. Its comprehensive features and benefits make it an essential platform for organizations looking to streamline 
their digital operations and deliver exceptional user experiences.

## What do you need to get started?
To get started with Acquia Site Factory, you will need:
1. **Subscription**:  First, you'll need to purchase a subscription to Acquia Site Factory. The subscription tier you 
choose will determine the level of support and features available to you.
2. **Setup and Configuration**: This includes configuring the Site Factory Administrative Console, which allows you to 
manage your sites and their configurations. If you need help, feel free to [reach out to us](https://www.merkle.com/dach/en/contact).
3. **Training and Onboarding**: Acquia provides training and onboarding services to help your team understand how to use 
the platform effectively. This can include tutorials, documentation, and support from Acquia's experts or via materials on their Academy.
4. **Local setup**: We suggest using Lando, free, open-source, cross-platform local development tool built on Docker. 

Some of the benefits using Lando's Acquia recipe are:
* It allows you to create a local environment that closely mirrors your Acquia hosting environment. This ensures that 
what you develop locally behave similarly when deployed to Acquia Cloud.
* You can easily pull websites to your local environment and push changes back to Acquia.
* It comes with built-in support for tools like Drush and Acquia CLI.

## Getting started with Lando and Acquia Site Factory
First, you need to install Lando on your local machine. You can download it from the [Lando website](https://lando.dev/).

Then, create a `.lando.yml` file in your project's directory. This file will define your local development environment. 
Here is an example configuration:
```yaml
name: my-project
recipe: acquia
config:
  acli_version: latest
  ah_application_uuid: null
  ah_site_group: null
  build:
    run_scripts: true
  cache: true
  composer_version: '2'
  inbox: true
  php: '8.3'
  xdebug: false
```
You can either create a file or start command `lando init` and follow the instructions on the screen. It is recommended 
to use `lando init` as it will also populate the `ah_application_uuid`, `ah_site_group` and `php` version for you.


{{< figure link="images/01-Lando-init-example.webp" caption="Lando init example" alt="Lando init example" >}}

Acquia recipe will spin up an approximation of the Acquia stack which consists of Apache web server, MySQL database server, 
Memcache and PHP. Lando also provides Mailhog service that catches and let's you inspect any outgoing e-mail locally.

There might be a case when you don't want some advanced parts of the stack to be used in local (for example Memcache).
Thanks to Lando's powerful configuration system, you can easily disable them; for example cache or inbox. 

Simply change `.lando.yml` to:
```yaml
recipe: acquia
config:
  cache: disable
  inbox: false
```