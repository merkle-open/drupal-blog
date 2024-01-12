---
title: Acquia Site Studio - Create components using UI
date: 2023-07-27
author: Danko Krstić
tags: ["acquia", "acquia-site-studio", "drupal-planet"]
---

## Components
Acquia Site Studio components provide a flexible layout system for editors and site builders. Components are mini templates with customized edit forms, offering flexibility in design. They can be added and blended on the Layout Canvas to craft new layouts.

Editors find them particularly valuable for creating pages where content and layout requirements defy a rigid template structure. These components encompass editable content, styles, and various settings. Component becomes a versatile asset, they can be reused on the same page or across different pages, each instance accommodating different content and settings.

The diagram below illustrates how the component builder facilitates the creation of both the layout of components and the forms that editors will use to edit content when added to a page.

{{< figure link="images/acquia-site-studio-component-builder-diagram.png" caption="Component builder diagram (illustration from Acquia)." alt="Acquia Site Studio - Component builder diagram" >}}
{{< figure link="images/acquia-site-studio-component-builder-visual.jpg" caption="Component builder - how it looks like in the system." alt="Acquia Site Studio - Component builder visual" >}}

The component layout and the component form are configuration. It can be deployed with other configurations. When a component is used on a page, the content added to the editable fields is stored as content within the Layout Canvas field. Before version 6.9 of Site Studio, the creation of components was only possible using Site Studio UI. Version 6.9 introduces custom components, components that can be created in code.

In this blog post, we will focus on creating components using Site Studio UI.

## Elements
If we think of components as page building blocks, then elements are building blocks of components. Upon installing Site Studio and activating the Site Studio elements module, a collection of elements becomes available for creating components. These elements play a crucial role in adding content, structure, and interactivity to the components. They span from fundamental base-level elements, such as paragraph elements, to more dynamic ones like sliders. Just as with components, Site Studio supports the development of custom elements, allowing the creation of specialized elements within custom Drupal modules.

* **Content elements** - Used to add content to a component or template.
* **Layout elements** - Used to add layout and structure to a component or template.
* **Media elements** - Used to add images, video, and other media to a component or template.
* **Interactive elements** - Used to add interactive devices to a component or template.
* **View elements** - Used to create templates for Drupal views.
* **Menu elements** - Used to create templates for Drupal menus.
* **Drupal core elements** - Used to add Drupal core components to a component or template.

## Create a component
In Site Studio we can create components using the component builder tool. In the next steps, we will create a simple editable component.

* Go to Site Studio > Components > Components > Add Component
* Enter the component name in the Title field.
* Enter category (This determines where the component is displayed on the Site Studio sidebar browser).
* Add component preview image.
* Enable inline editing (Allowing the component's content to be edited directly on the website via Page Builder).

### Create the component layout
In the Layout Canvas field we control how components will be displayed.

1. Click on the plus button and add a paragraph element from the sidebar browser.
2. Double-click on the paragraph element will open the paragraph form where we can manage basic settings and styles for components.
   1. Settings 
      1. Paragraph text (Default value for paragraph component)
      2. Custom style (Attach predefined styles for paragraph component)
         {{< figure link="images/acquia-site-studio-paragraph-element-settings.png" caption="Settings for paragraph element." alt="Acquia Site Studio - Settings for paragraph element" >}}
   2. Styles
      1. If we have styles that apply only to this component, we can add them here. Click on the properties button and add the background color.
         {{< figure link="images/acquia-site-studio-custom-style-background-color.png" caption="Add custom style background color" alt="Acquia Site Studio - Custom style background color" >}}
3. We also can add additional wrappers like containers or rows and columns. For those elements, we can also set style options.

### Create the component form
The component form is the place where content editors manage component content, settings, and styles.
We can create a component form in the component form builder  section. We can live-preview all changes in the component form preview section below.

1. Click on the plus button on the component form builder  to open the Site Studio sidebar browser.
2. If not selected, click on Fields in the menu at the top of the sidebar.
3. Drag a plain text area field element onto the component form builder. 
4. Double-click on the field in the component form builder to open its settings.
   1. Here we can configure the field and set the field name and the field machine name.
      {{< figure link="images/acquia-site-studio-field-configuration.png" caption="Plain text field configuration." alt="Acquia Site Studio - Plain text field configuration" >}}
5. After we click on the Apply button and save the changes, we can see that the field on the component form builder displays a machine name as a token. We will use this token to link the form field to the component layout.
   {{< figure link="images/acquia-site-studio-component-form-builder-paragraph.png" caption="Component form builder for paragraph text." alt="Acquia Site Studio - Component form builder for paragraph text" >}}

### Link the component form to the component layout
In this last step, we need to connect the component layout (display) and the component form (entry form).

1. Double-click on the paragraph element on the Layout Canvas to open its settings.
2. Click on the plus icon to switch all fields into variable mode. This allows you to enter tokens into the fields.
3. Enter the token (this is the machine name of your plain text area field) in the paragraph text field. Ensure you use square brackets around the token. 
4. Click on the plus icon to toggle out of the variable mode.
5. Click Apply.
   {{< figure link="images/acquia-site-studio-form-builder-paragraph-link.png" caption="Connection of component layout (display) and component form (entry form) via token." alt="Acquia Site Studio - Connection of component layout (display) and component form (entry form)" >}}

## Add component to a page
Now we are ready to use the newly created component.

1. Create or edit a page that has the Layout Canvas.
2. Click on the plus button to open the sidebar browser.
3. Click on the components tab.
4. Drag your new component onto the Layout Canvas.
5. Double-click on the component to edit its settings.
6. Add some text to the plain text area.
7. Preview your page to see your component applied.


{{< figure link="images/acquia-site-studio-add-paragraph-component-to-page.png" caption="Add paragraph component to Layout Canvas." alt="Acquia Site Studio - Add paragraph component to Layout Canvas" >}}
{{< figure link="images/acquia-site-studio-edit-paragraph-component.png" caption="Edit paragraph component." alt="Acquia Site Studio - Edit paragraph component" >}}

## Let's rock a Site Studio project together!
Merkle offers a Site Studio starter kit! Go live with Acquia at your pace with the package that suits your needs (the packages can be built on top of each other).
* **Small** – we go live fast in a few weeks by using Site Studio’s predefined components with only little customisations.
* **Medium** – after a workshop we modify part of Site Studio’s predefined components according to the agreed adjustments.
* **Enterprise** – based on a discovery and design sprints we adjust the UI Kit components according to the design.
* **Custom** – we create individual Site Studio components for you that meet all your requirements.

[Get in touch with us!](https://www.merkle.com/dach/en/contact)
