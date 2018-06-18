---
title: 03. Installing plugins
permalink: installing-plugins.html
---

# How to install plugins

There are two main ways to add new WordPress plugins to our architecture.

1. Use [Composer] and [Wpackagist](https://wpackagist.org/) (preferred).

    Whenever possible we should leverage the qualities of Composer and install the plugin as its dependencies.
    
    1. Navigate to the [Wpackagist](https://wpackagist.org/) website.
    1. Use the searchbox to find the plugin you want to install. Wpackagist does a great job in having most of WordPress ecosystem there.
    1. Run the following composer command in the root of the project to add the plugin to your dependencies and install it, for example:  
    ```
    composer install "wpackagist-plugin/query-monitor":"3.0.1"
    ```
    1. Commit your `composer.json` and `composer.lock` to the repository

1. For premium (or other plugins which you can't install via Composer) you should:
    1. Install the plugin using the regular WordPress way (via admin, uploading Zip file or manually).
    1. Exclude your plugin directory in `.gitignore` file by adding the path similar to `!/public/core/plugins/your-plugin`
    1. Commit `.gitignore` and plugin contents into the repository.
    
It is worth mentioning that you can use composer for adding any other vendor library to your code stack.