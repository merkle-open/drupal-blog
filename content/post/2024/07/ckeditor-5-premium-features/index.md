---
title: CKEditor 5 Premium Features
date: 2024-07-10
author: Danko Krstić
tags: ["ckeditor5", "drupal", "drupal-planet"]
---
CKEditor 5 is a rich text editor that offers a modern editing experience with real-time collaboration capabilities, intuitive interfaces, and robust functionality. CKEditor 5 is built on an entirely new framework based on Node.js. This editor can be integrated into Drupal CMS using “[CKEditor 5 Premium Features](https://www.drupal.org/project/ckeditor5_premium_features)” Drupal module, providing users with a streamlined content editing experience.

Using CKEditor 5 premium features requires a license. For testing purposes, there is a trial version which includes subscription of 30 days at no cost. AI Assistant and Spell and grammar check (WProofreader) also require~~s~~ licenses to be used.

## Collaboration
{{< figure link="images/001-collaboration.webp" caption="CKEditor 5 Collaboration functionality" alt="CKEditor 5 Collaboration functionality interface" >}}

Multiple users can work on the same rich text document in real time. Any changes on one editor are immediately visible on all other open editors. Collaboration Features:

- **Track changes**  
Make suggested edits.

- **Comments**  
Discuss the content.

- **Revision History**  
See what changes were made and compare and restore previous versions of the content.

- **Real-time Collaboration**  
Allow multiple users to edit simultaneously.

A customizable notification system keeps you informed whenever someone mentions you in a document, comments, replies to you, or accepts or rejects suggestions. You can also integrate it with your own plugin to receive notifications via email.

## AI Assistant
{{< figure link="images/002-ai_assistant.webp" caption="CKEditor 5 AI Assistant tool" alt="CKEditor 5 AI Assistant tool" >}}

With this feature CKEditor became a powerful tool to generate, translate or summarize content. It supports some of the leading AI models like OpenAI GPT-3.5, OpenAI GPT-4, Azure OpenAI service or Amazon Bedrock service. You can select text, and use predefined commands, ask AI to change the tone and style, fix grammatical errors, make it longer or shorter and much more. The AI answers can be adjusted by using specific model or by params like “temperature” and “top_p”.

## Productivity pack

Productivity pack is a set of plugins that makes content editing more efficient and easier. It includes the following features:

- **Slash Commands**  
Using “/” gives you access to the list of predefined or custom commands.

- **Document Outline**  
In right side bar shows document headings.

- **Table of contents**  
Inserts a linked table of contents.

- **Format Painter**  
Copies text formatting and styles and applies it to a different part of the content.

- **Paste from Office Enhanced**  
Provides copy-pasting from MS Word and Excel. Formatted text, complex tables, media, and layouts are retained – turning MS Office content into clean HTML.  
[Complete list of supported formatting](https://ckeditor.com/docs/ckeditor5/latest/features/pasting/paste-from-office-enhanced.html)

- **Templates**  
Create pre-designed content structures and insert it in a document.

- **Case change**  
Quick change of letter case.

## WProofreader spelling and grammar checker
&nbsp;
&nbsp;
&nbsp;
{{< figure link="images/003-wproofreader.webp" caption="CKEditor 5 WProofreader spelling and grammar checker tool" alt="CKEditor 5 WProofreader spelling and grammar checker tool" >}}

WProofreader for CKEditor 5, developed by [WebSpellChecker](https://webspellchecker.com/), is a sentence correction tool, enhancing it with spelling and grammar check functionality. Its core features include:

- Multilingual proofreading in as-you-type and in-dialog modes for 20+ languages;

- Spelling autocorrect and text autocomplete suggestions;

- Style guide suggestions with predefined rules for non-inclusive and profane language;

- User and organization-level dictionaries;

- Specialized medical and legal spelling dictionaries for English, German, Spanish and French;

- Compliance with WCAG 2.1 and Section 508 accessibility standards.

## Export to PDF & MS Word

With one click you can export content to .pdf or .docx file. This feature firstly collects HTML from editor and then adds default editor content styles combined with the styles provided by you in the configuration. It then sends them to CKEditor Cloud converter service. The service generates files and returns them to the user browser. 

## Import from MS Word
Import Microsoft Word .docx or .dotx document formats in CKEditor 5. Formatting, Comments and Track Changes from the Word document will be retained in CKEditor. 

## Multi-level lists
Legal style numbering feature (1, 1.1, 1.1.1). Makes it easier to structure complex documents. This feature is fully compatible with paste from Office and import from Microsoft Word.


&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;

In addition to all of the above, plugin-based architecture, great UI and UX makes CKEditor 5 cutting edge tool for content creation and editing. Integrated in Drupal, makes life easier to both developers and content editors.