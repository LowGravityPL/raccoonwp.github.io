---
title: 02. Installation
permalink: installation.html
---

# Installation
  1. Ensure that you meet the minimum requirements:
      - [PHP](https://secure.php.net/) 7.0 or newer
      - [PHP Composer](https://getcomposer.org/)
      - [Node and NPM](https://nodejs.org/) (optional if you do not want develop theme)
  1. Use composer to create a project:
      ```
      composer create-project lowgravitypl
      ```
      [todo: create a package on packagist]
  1. Set up your environment config file:
      - copy .env.sample
      - put salts in [create salts url]
      - Add db config info
      - set wp urls
      [todo: more info needed, rewording]
  1. After you set everything up you need to adjust your web server's (usually Apache or nginx) configuration and point your web root to the `public/` directory. 
  [example? or too specific?]