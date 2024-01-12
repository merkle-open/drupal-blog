---
title: Acquia Site Studio - get started!
date: 2023-07-24
author: Danko Krstić
tags: ["acquia", "acquia-site-studio", "drupal-planet"]
---

## Acquia Site Studio
Site Studio, formerly known as Cohesion, is an Acquia solution for Drupal to build a low-code and component-based website. The tool offers a user-friendly drag-and-drop interface, making it easy for non-technical people to effortlessly create and modify web pages. Adding content, updating content, and making simple design adjustments are all easily achievable with this solution. The key features are:

* Low-code / no-code
* Component-based approach
* Powerful visual user interface

Traditional enterprise-grade websites typically involve collaboration among teams specializing in software, design, and digital marketing, with marketing often having to wait until the final stages to contribute content. Site Studio, however, empowers marketers and content writers by providing controlled access for direct updates and edits to both content and layouts. Whether it's swapping an image with a text box or making other adjustments, marketers can efficiently execute these changes. The visual interface and in-context editor enable writers to edit content directly on the website.

## Benefits of using Acquia Site Studio
* **UI Kit** - Site Studio provides a [UI Kit](https://sitestudiodocs.acquia.com/6.3/user-guide/site-studio-primitives-uikit) with over 50 predefined components which you can start using immediately like Text, Image, Slider, Accordion, etc.
* **Drag-and-drop interface** - Site Studio provides an excellent content editing user interface for adding components or templates in the layout by simply dragging and dropping.
* **Page builder** - A powerful visual user interface and in-context editor that lets you edit content directly on the website.
* **Layout Canvas** - Creation of component-based pages also from the backend to get an abstracted, structural view of the components of the page.
* **Enforcing Brand Guidelines** - Brand consistency by defining colors, fonts, and styles on the component level.
* **Helper Library** - Save layout compositions as reusable ”helpers” to speed up page creation. Save any component or group as a helper to view in your helper library.
* **Low-code easy to use** - Low code makes it appealing to users with less to no knowledge of building Drupal pages.
* **Responsive ready** - Empowers users to preview their layout in various devices just by changing the settings of the device aspect ratios.
* **Custom Components** - Once built for any frontend technology (including React, etc.) they can be used everywhere.
* **Composable Digital Experiences** - Use of reusable components from the component library and shared across different websites.
* **Accelerate development** - The development process can be accelerated because of the reusability and low-code nature.
* **Sync Package Manager** - Package templates, components, styles, and configurations to deploy from development to production or export and import elements across different sites.
* **Personalization** - Pair Acquia Site Studio with [Acquia Personalization](https://www.acquia.com/drupal/personalization) to unify customer content and profile data from multiple sources to any channel or device.
* **Easy integration** - Easy integration of [Acquia DAM](https://www.acquia.com/products/acquia-dam) and [Acquia PIM](https://www.acquia.com/solutions/product-information-management).

## Edit content with Acquia Site Studio
### Layout Canvas
As a site builder, your task involves assembling diverse blocks to construct your design effectively. In the context of websites, a component can take the form of a text block, an image, a featured snippet, a live Twitter feed, a header, a footer, and much more. These components collectively contribute to the completion of your website design.

Layout Canvas | Layout Canvas edit overaly
:---: | :---:
{{< figure link="images/acquia-site-studio-layout-canvas-backend.png" alt="Acquia Site Studio - Layout Canvas" >}} | {{< figure link="images/acquia-site-studio-layout-canvas-backend-edit.png" alt="Acquia Site Studio - Layout Canvas Edit Overlay" >}}

### Page Builder
When users are logged in and on a page that utilizes Acquia Site Studio and a layout canvas, they will see a Page Builder button on the admin toolbar. Activating the page builder mode grants users the ability to seamlessly add, edit, reposition, delete, duplicate, and save content as components. Users can also save the entire page layout. Ensuring consistency, new components or elements can be easily added via the off-canvas components drawer on the left side. This approach eliminates the need for users to relearn how to add components, resulting in an enhanced page-building experience.

Acquia Site Studio's innovative visual page builder truly embodies the concept of "what you see is what you get," offering content editors an unparalleled and simplified page-building experience!

Page Builder | Page Builder edit overaly
:---: | :---:
{{< figure link="images/acquia-site-studio-page-builder.png" alt="Acquia Site Studio - Page Builder" >}} | {{< figure link="images/acquia-site-studio-page-builder-edit.png" alt="Acquia Site Studio - Page Builder Edit Overlay" >}}

## Getting started with Acquia Site Studio
1. Install Acquia Site Studio module and theme via composer. Site Studio will install along with several module dependencies from drupal.org
    ```
    composer require acquia/cohesion:^7.0 acquia/cohesion-theme:^7.0
    ```
2. Enable Site Studio core and all dependent modules together except for the "Site Studio example custom element" and "Site Studio breakpoint indicator" module as shown below:
   {{< figure link="images/acquia-site-studio-enable-in-drupal-backend.png" caption="Enable in Drupal backend" alt="Acquia Site Studio - Enable in Drupal backend" >}}
4. Connect to the Site Studio API
   1. Navigate to Site Studio > Configuration > Account settings
   2. Enter your API key
   3. Enter your Agency key
   4. Your Site ID and API server URL will be pre-populated
   5. Click Save and import assets
   6. This will connect your website to the API and begin importing required assets. Once this has completed, you will be able to use Site Studio.
      {{< figure link="images/acquia-site-studio-api-account-settings.png" caption="API account settings" alt="Acquia Site Studio - API account settings" >}}
5. Enable the Site Studio minimal theme
   1. Click on Appearance in the Drupal navigation
   2. Click on Install and set as default Site Studio minimal theme.
6. Configure image and media browsers
   {{< figure link="images/acquia-site-studio-select-media-browsers.png" caption="Media Browser selection" alt="Acquia Site Studio - Media Browser selection" >}}
7. Navigate to Site Studio > Configuration > System settings.

   The options shown depend on the media browser modules you have enabled. Site Studio supports the Drupal core Media library as well as contributed modules  IMCE and Entity Browser for managing images.
   1. Adding the layout canvas field to content entities
   2. Navigate to Structure > Content types > (Select a content type)
   3. Click on Manage fields
   4. Click Add field
   5. Select Layout canvas in the Add a new field drop-down
      {{< figure link="images/acquia-site-studio-adding-layout-canvas-field.png" caption="Layout Canvas field" alt="Acquia Site Studio - Layout Canvas field" >}}

**You are ready to start using Site Studio!**

> Merkle offers a Site Studio starter kit! Go live with Acquia at your pace with the package that suits your needs (the packages can be built on top of each other).
> * **Small** – we go live fast in a few weeks by using Site Studio’s predefined components with only little customisations.
> * **Medium** – after a workshop we modify part of Site Studio’s predefined components according to the agreed adjustments.
> * **Enterprise** – based on a discovery and design sprints we adjust the UI Kit components according to the design.
> * **Custom** – we create individual Site Studio components for you that meet all your requirements.
>  
> --> [Get in touch with us!](https://www.merkle.com/dach/en/contact)
