---
title: 01. Getting started
layout: default
---

# RaccoonWP
**If you find any issues let us know**

Raccoon is a modern architecture stack and a starter theme for [WordPress](https://wordpress.org/). 

The stack is based on the Composer on the backend. Node.js with Webpack are used on the frontend. 
This composition allows for a quick and efficient development using the tools which are **state of the art in 2019.**  

You should use it as your boilerplate/starter kit to obtain **optimal architecture with performance, extensibility and security** in mind.

Raccoon is best suited for fresh projects (but there is no problem in implementing it into existing ones with some effort).

### Technical Requirements
- [WordPress](https://wordpress.org/) 4.0+ (or 4.8 if You use extended CPTs) 
- [PHP](https://secure.php.net/) 7.1.3 or newer
- [PHP Composer](https://getcomposer.org/)
- [Node and NPM](https://nodejs.org/) (required only if you want to use our theme as well)

### Features
- Architecture:
    - [PHP Composer](https://getcomposer.org/) support.
    - [WordPress](https://wordpress.org/) Core as a dependency.
    - Full [Docker](https://github.com/LowGravityPL/raccoon-docker) image for your local development
    - Support for [Wp-Cli](https://wp-cli.org/).
    - Better directory structure and more secure than default WordPress install.
    - Environment-based configuration.
    - Proper project data management.
    - Ability to disable plugins per environment.  
    - Internationalization built in from the beginning.    
    - [Coming soon] Multisite not tested yet! Though it should work without issues.
    - [On the roadmap] Unit tests
    - [On the roadmap] E2E tests
    - [On the roadmap] Progressive Web App and Service Worker 
- Theme:
    - Customizable theme build process based on newest [Webpack 4.28](https://webpack.js.org/) with all its features
    like dead code elimination, bundle analysis, watch process and more.
    - Flexible CSS: Plain SASS by default / Bootstrap 4 / Foundation 5 / Bourbon/Neat or anything else (check [recipes section](https://raccoonwp.lowgravity.pl/recipes)).
    - Modern JS: all newest features like ES6, modules, spreads, destructuring objects and arrays etc.
    - NPM: node package manager allowing to import various 3rd party libraries into the project.
    - uses Twig (default) or Blade templating (or you can go old plain WordPress way).
    - Vue? React? We got you covered, check [recipes section](https://raccoonwp.lowgravity.pl/recipes).
    - [Gutenberg](https://wordpress.org/gutenberg/) support. 
    - [On the roadmap] Child theme support.
    
    See our [recipes section](/recipes) to see how to tweak the project to your needs.


### License
[MIT](LICENSE.md) © [LowGravity.pl](https://lowgravity.pl)

----
### Brought to you by [LowGravity.pl](https://lowgravity.pl)
We are the team of experienced developers and designers working with various clients around the globe. We have worked
on small personal websites as well as large scale enterprise ones. 

Our main focus is code quality and performance, We help small and big teams making their workflow, projects and
infrastructure be more robust, performant and secure. 

Our area of expertise focuses mostly on WEB technologies but we are not afraid of other challenges.

#### Contributors
- [Kamil Grzegorczyk](https://kamilgrzegorczyk.com)
- [Lucas Grzegorczyk](https://github.com/furai)
- Artwork by [Izabela Grzegorczyk](https://www.behance.net/IzaGrzegorczyk)
