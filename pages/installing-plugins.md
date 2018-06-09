---
title: 03. Installing plugins
permalink: installing-plugins.html
---

# How to install plugins

There are two ways of installing plugins:

1. Use Composer and [wpackagist](https://wpackagist.org/) (preferred).

    Whenever possible we should leverage the qualities of Composer and install the plugin as its dependencies.
    
    - navigate to wpackagist website
    - find the WP plugin you want to install
    - run the installation command like 
    ```$xslt
    composer install "wpackagist-plugin/query-monitor":"3.0.1"
    ```
    - commit your `composer.json` and `composer.lock` to your repository

1. For premium or other plugins you cannot install via Composer you should:
    - install the plugin in the regular WordPress way (via admin, uploading Zip file or manually)
    - exclude your plugin directory in `.gitignore` file by adding the path like `!/public/core/plugins/your-plugin
    - commit `.gitignore` changes as well as your plugin contents into the repository