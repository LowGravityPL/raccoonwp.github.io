---
title: 02. Installation
permalink: installation.html
---

# Installation
To start using RaccoonWP please follow the steps below:
  1. Ensure that you meet the minimum requirements:
      - [PHP](https://secure.php.net/) 7.0 or newer
      - [PHP Composer](https://getcomposer.org/)
      - [Node and NPM](https://nodejs.org/) (optional if you do not want develop theme)
  1. Use composer to create a project by running following command:
      ```
      composer create-project -s dev lowgravitypl/raccoonwp
      ```
  1. Set up your environment config file:
      1. Copy `.env.exmaple` file and name it `.env`
      1. Navigate to [https://lowgravity.pl/salts.php](https://lowgravity.pl/salts.php) to generate salts 
      and paste them into your `.env` file.
      1. Add all environment configuration details like DB connection details or environment type.
      1. Set proper site and home URLs.
  1. Adjust your web server's (usually Apache or nginx) configuration 
  and point your web root to the `public/` directory. 
  1. (optionally) Go to `/RaccoonWP/configuration` directory and adjust your custom environment configuration there.
  1. Visit the url in the browser.
  
### Theme development
If you want to use our starter themes please follow the steps mentioned in [theme development documentation](/theme-development).