---
title: How to migrate Back Office pages to Symfony 3
menuTitle: Migration guide
chapter: true
weight: 20
---

# How to migrate Back Office pages to Symfony 3

Migrating a legacy page in PrestaShop requires working on three parts of the application: templates, forms and controllers which contain the business logic.

## Strategy / To-do List

This is the list of items that usually need to be done in order to complete the migration of a legacy controller.

- Creations
  - Create `PrestaShopBundle/Controller/<path>/<Your>Controller`
  - Create related actions (functions matched to URIs)
  - Declare routing in `config/routing/admin/routing_*.yml` file
  - Create Symfony form types for each form available in pages
  - Create and configure Javascript (using Webpack/ES6) file
  - Create every twig blocks in `views/<path>/*.html.twig`
  - Implement Forms submission
  - Implement Forms validation
  - If required, implement (request) Parameters update
  - Check Error Handling
  - Checks permissions and demo mode constraints
  - Re-introduce hooks (and document the missing one if you can't for a good reason)
  - Complete `Link` class to map PrestaShop menu to the new page
- Deletions
  - Remove the old controller in `controllers/admin/Admin*.php`
  - Remove related old templates (in `admin-dev/themes/default/template/controllers/*`)

## Contents of this guide

{{% children %}}
