# Plone Cheat Sheet
A collection of useful tips and advices from the Plone community, to help the webmaster and developer.

## Table of Contents
  - [Plone CMS](#plone-cms)
    - The big picture 
    - Installation 
    - Site setup
    - Editing interface
    - Admin interface
    - Content types
  - [Buildout](#buildout)
  - [Plone Front-end development](#plone-front-end-development)

## Plone CMS
### The big picture
TODO

### Installation
TODO

### Site setup
TODO

### Editing interface
TODO

### Admin interface
TODO

### Content types
A Plone-based application is structured around content types.
There are default content types provided OOTB to cover most use cases for simple sites and regular editorial site sections: Page, News Item, Image, File, Folder, Collection.
Limiting your usage to default types means less bugs on the path forward (i.e. upgrades).

Use Collections to get a `smart listing` feature for free. Can be combined with Portlets.

#### Dexterity-based default content types
You can start using the new [Dexterity-based default content types ](https://github.com/plone/plone.app.contenttypes), developed for Plone 5, on a Plone 4.3.3 setup. This way, you get these last 5 years' improvements from the Plone community, and get ready when Plone 5 arrives.

Some advantages of using Dexterity-based types:
  * Dexterity `behaviours` such as `RichText`, `LeadImage`, event `start date` & `end date` fields, can be reused for your content types, even TTW. See _Dexterity content types control panel_.
  * It is possible to define a new content type TTW, if you need to.
  * Content Internationalization is supported via the new internal framework `plone.app.multilingual` with the `plone.app.multilingualbehaviour` package for the Dexterity integration layer.


#### Policy settings for content types
You can decide *if/how* your types are searchable. Make sure your search results are filtered, and do not show unrelevant stuff. See the _Search control panel_.

You can decide *if/how* your types are exposed in the site navigation. Make sure the navigation tools (portal tabs, navigation portlet) do not show unrelevant stuff. See the _Navigation control panel_.

#### Resources

| Title | Link |
| ----- | ---- |
| Plone Documentation - Dexterity | http://docs.plone.org/external/plone.app.dexterity/docs/index.html |
| Todo list application tutorial | http://tutorialtodoapp.readthedocs.org/en/latest/ |
| Multilingual sites in Plone (talk) | http://fr.slideshare.net/bloodbare/multilingual-sites-in-plone |
