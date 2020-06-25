.. _configuation:

*************
Configuration
*************

There are a number of options for configuring your site's look and feel.
All configuration options are passed with the ``html_theme_options`` variable
in your ``conf.py`` file. This is a dictionary with ``key: val`` pairs that
you can configure in various ways. This page describes the options available to you.

Configure project logo
==============================

To add a logo that's placed at the left of your nav bar, put a logo file under your
doc path's _static folder, and use the following configuration:

.. code:: python

   html_logo = "_static/logo.png"

Configure social media buttons
==============================

If you'd like social media buttons to show up to the right of your nav bar, use the
following configuration:

.. code:: python

   html_theme_options = {
     "github_url": "https://github.com/<your-org>/<your-repo>",
     "twitter_url": "https://twitter.com/<your-handle>",
   }

Adding external links to your nav bar
=====================================

You can add external links to your navigation bar. These will show up to the right
of your site's main links, and will have a small icon indicating that they point to
an external site. You can add external links to the nav bar like so:

.. code:: python

   html_theme_options = {
     "external_links": [
         {"name": "link-one-name", "url": "https://<link-one>"},
         {"name": "link-two-name", "url": "https://<link-two>"}
     ]
   }


Hiding the previous and next buttons
====================================

By default, each page of your site will have "previous" and "next" buttons
at the bottom. You can hide these buttons with the following configuration:

.. code:: python

   html_theme_options = {
     "show_prev_next": False
   }


Add an Edit this Page button
============================

You can add a button to each page that will allow users to edit the page text
directly and submit a pull request to update the documentation. To include this
button in the right sidebar of each page, add the following configuration to
your ``conf.py`` file:

.. code:: python

   html_context = {
       "github_user": "<your-github-org>",
       "github_repo": "<your-github-repo>",
       "github_version": "<your-branch>",
       "doc_path": "<path-from-root-to-your-docs>",
   }

You should also enable the edit option in your 'html_theme_options':

.. code:: python

   html_theme_options = {
       "use_edit_page_button": True,
   }

Configure the search bar position
=================================

To modify the position of the search bar, change the following variable in
your configuration file ``conf.py``. Possible options are 'navbar' and 'sidebar'.

By default the search bar is positioned in the sidebar since this is more
suitable for large navigation bars.

.. code:: python

    html_theme_options = {
        "search_bar_position": "navbar"
    }

Configure the search bar text
=============================

To modify the text that is in the search bar before people click on it, add the
following configuration to your ``conf.py`` file:

.. code:: python

   html_theme_options = {
       "search_bar_text": "Your text here..."
   }


Google Analytics
================

If the ``google_analytics_id`` config option is specified (like ``UA-XXXXXXX``),
Google Analytics' javascript is included in the html pages.

.. code:: python

   html_theme_options = {
       "google_analytics_id": "UA-XXXXXXX",
   }


Changing pages with keyboard presses
====================================

By default, ``pydata-sphinx-theme`` allows users to move to the previous/next
page using the left/right arrow keys on a keyboard. To disable this behavior,
use the following configuration:

.. code-block:: python

   html_theme_options = {
     "navigation_with_keys": False
   }
