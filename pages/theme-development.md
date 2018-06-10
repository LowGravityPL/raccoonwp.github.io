---
title: 04. Theme development
permalink: theme-development.html
---

# How to build a theme?

RaccoonWP comes with a starter theme. By default it comes with Twig templating engine support.
If you are not a fan of Twig you can replace it with Blade or use plain old WordPress templating.

See our [recipes section](/recipes) to see how to tweak the project to your needs.

### Initial set up
In order to develop theme you need to have [Node and NPM](https://nodejs.org/) installed in the system.

1. Navigate to theme directory by tpying `cd public/core/themes/raccoon-theme` in your terminal
1. Run `npm install` command.

### Configuration 
More information coming soon.
- webpack config
- eslint config

### Available terminal commands
- `npm run watch`  
Runs watch process which builds assets on the fly using browsersync for reloading changes. 
It does Hot Module Replacement too if your code supports that.
- `npm build`  
Builds development version of the assets
- `npm run build:prod`  
Run production build
- `npm run lint`  
Run eslint javascript linting process

### Child theme
At the moment theme does not have official child theme support. 

### Customization
See our [recipes section](/recipes) to see how to tweak the project to your needs.
