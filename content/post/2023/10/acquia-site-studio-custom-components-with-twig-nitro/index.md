---
title: Acquia Site Studio - Custom components with Twig Nitro
date: 2023-10-10
author: Danko Krstić
tags: ["acquia", "acquia-site-studio", "drupal-planet"]
---

This is a follow-up of the [Acquia Site Studio - Custom components](/post/2023/10/acquia-site-studio-custom-components/) blog post. We are going to use Nitro in the Twig templates.

## Frontend integration with Twig Nitro Bridge
Twig is a modern template engine for PHP used by Drupal. [Twig Nitro Bridge](https://www.drupal.org/project/twig_nitro_bridge) is the extension to use the [Nitro](https://github.com/merkle-open/generator-nitro) components in Drupal's Twig templates. Nitro is a Node.js application for frontend development with a tiny footprint. It provides a flexible structure to develop frontend code, even in a large team.
We are going to use Twig Nitro Bridge to integrate frontend components into Drupal Twig template.

## Site Studio and Twig Nitro integration
Steps to integrate Site Studio with Twig Nitro:

1. Create sub-theme - Site Studio comes with **Site Studio minimal Drupal**. The first step is to create a custom sub-theme based on Site Studio minimal theme.
2. Add [Twig Nitro Bridge Drupal module](https://www.drupal.org/project/twig_nitro_bridge)
   ```
   composer require drupal/twig_nitro_bridge
   ```
   It will also add [Twig Nitro library from GitHub](https://github.com/merkle-open/twig-nitro-library) as a dependency.
3. Create a THEME_NAME.libraries.yml file in your sub-theme and include frontend's JavaScript and CSS files.
   ```
   terrific:
     version: 1.x
     css:
       theme:
         /assets/css/ui.min.css: {}
     js:
       /assets/js/vendors.min.js: { weight: -200 }
       /assets/js/ui.min.js: { weight: -100 }
   ```
   If you need help, check the [.libraries.yml documentation](https://www.drupal.org/node/2216195)
4. Include the library in your THEME_NAME.info.yml file and set `cohesion` param to `true` (enable Site Studio for sub-theme)
   ```
   libraries:
     - nitross/terrific
   
   cohesion: true
   ```
   If you need help, check the [.info.yml documentation](https://www.drupal.org/docs/develop/theming-drupal/defining-a-theme-with-an-infoyml-file)

## Using frontend components in Site Studio custom components
The markup below shows an example of the Site Studio teaser component created by calling the frontend `teaser` component in the `teaser.html.twig` template file.
```
{% set teaserData = {
  title: field.teaser_title,
  text: format_wysiwyg(field.teaser_text['#text'], field.teaser_text['#textFormat'], ''),
  button: {
    text: field.teaser_button_text
  },
  image: {
    image: {
      alt: teaser_alt_text,
      src_small: teaser_url,
      src_small2x: teaser_url,
      src_medium: teaser_url,
      src_large: teaser_url,
      src_extralarge: teaser_url
    }
  },
  lazyload: true,
  colDefinition: field.teaser_width
}%}
 
{% component 'teaser' teaserData %}
```

By integrating Site Studio and Twig Nitro, we get an improved and very powerful system for content creation and editing. On the one hand, we eliminate one of the shortcomings of Site Studio, which can be a very complex system of creating components using the UI. On the other hand, we use a very advanced content management interface provided by Site Studio.

**In short, the benefits of using Site Studio with Twig Nitro:**

1. Site Studio drag-and-drop interface for content creation and editing.
2. Site Studio Page Builder - preview real-time changes instantaneously.
3. Building custom components in code removes the need to create components using the Site Studio UI interface which can be very complex and demands frontend developers that have experience with Site Studio.
4. Using Twig Nitro, we are enabling the frontend team without the need to change anything in their usual working process.

## Let's rock a Site Studio project together!
Merkle offers a Site Studio starter kit! Go live with Acquia at your pace with the package that suits your needs (the packages can be built on top of each other).
* **Small** – we go live fast in a few weeks by using Site Studio’s predefined components with only little customisations.
* **Medium** – after a workshop we modify part of Site Studio’s predefined components according to the agreed adjustments.
* **Enterprise** – based on a discovery and design sprints we adjust the UI Kit components according to the design.
* **Custom** – we create individual Site Studio components for you that meet all your requirements.

[Get in touch with us!](https://www.merkle.com/dach/en/contact)
