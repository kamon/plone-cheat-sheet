# Plone Cheat Sheet
A collection of useful tips and advices from the Plone community, to help the webmaster and developer.

## Table of Contents
  - [Plone CMS](#plone-cms)
    - Installation 
    - Site setup
    - Editing interface
    - Admin interface
    - Content types
  - [Buildout](#buildout)
  - [Plone Front-end development](#plone-front-end-development)

## Plone CMS

### Installation
The recommended way for installing Plone is [Buildout](#buildout).
There is an installer, which itself is based on Buildout.

Alternative installation methods:
* [PloneDev.Vagrant](https://github.com/plone/plonedev.vagrant) is a kit for setting up an easy to use development environment for Plone in a hosted virtual machine.
* [Plock](https://github.com/plock/plock) is a solution proposed by Alex Clark to allow installing Plone via `pip install Plone`.

### Site setup
TODO

### Editing interface
TODO

### Admin interface
Plone has a rich featured interface for administrators, which includes `Portlets` and `Control Panels`.
There is also a configuration registry, used by Plone add-ons to store their configuration data.

#### Quick access to some useful parts of the interface

| To access | Do |
| --------- | -- |
| The Portlets interface | Add `/manage-portlets` to the URL of your current context |
| The Control Panels space | Visit http://url-to-your-site/`plone_control_panel` |
| The configuration registry | Visit http://url-to-your-site/`portal_registry` |

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

## Buildout
