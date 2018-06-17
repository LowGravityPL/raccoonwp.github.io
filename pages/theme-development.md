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

1. Navigate to theme directory by typing `cd public/core/themes/raccoon-theme` in your terminal
1. Run `npm install` command.

### Theme structure (rough overview, some files and dirs were omitted for readability)
```
├── app                            # main theme directory
│   ├── base                       # basic/core functionalities
│   │   ├── lib                    # a place for classes/helpers
│   │   ├── setup                  # files containing theme setup functions like assets enqueue, sidebars, menus
│   ├── data-helpers               # a place where you should put your data fetching functions (only theme related ones!)
│├── templates                     # directory for page/component templates
│└── translations                  # this is where you should put your translation files
├── assets                         # raw assets directory
│   ├── fonts
│   ├── images
│   ├── other
│   ├── scripts
│   │   └── app.js                 # main javascript file (webpack entry point)
│   └── styles
│       └── app.scss               # main sass file
├── build-util                     # all your webpack configuration
│   ├── common                     # common webpack configuration (shared between modes)
│   ├── helpers                    # webpack config helpers
│   ├── modes                      # webpack mode configs (prod, dev etc.)
│   ├── user.config.example.js     # example file for user configuration
│   ├── watch.js                   # watch mode script
│   └── webpack.config.js          # main weboack config file
├── dist                           # contains all processed, production-ready assets.
├── page-templates                 # this is where you should put your page tempaltes
└── package.json                   # contains your npm dependencies and runs webpack scripts
```

### Configuration 
More information coming soon.
#### Webpack config
We have tried to make webpack configuration clean and readable. 
Webpack itself came a long way since 1.x version and it gets better in its documentation and configuration.

Unfortunately there is still a certain learning curve to grasp how its really working.

Having that in mind we have created `user.config.js` file which exposes most important configuartion aspects.

How to use it?
1. Please copy `public/core/themes/raccoon-theme/build-util/user.config.example.js` and name the new file `user.config.js`.
1. Adjust the configuration to fit your project / environment. The most important setting may be `devUrl` which
is nothing else than local URL of the website on your local environment.

#### Eslint config
By default we use very soft linting rules as those should be defined by you and your team. 
You can configure the way your script files are getting linted. 

In order to do that edit the `public/core/themes/raccoon-theme/.eslintrc.js` file. 
Please follow [the official eslint documentation](https://eslint.org/docs/user-guide/configuring) for all available options.

### Available terminal commands
- `npm run watch`  
Runs watch process which builds assets on the fly using browsersync for reloading changes. 
It does Hot Module Replacement too if your code supports that.

- `npm build`  
Builds development version of the assets
  
- `npm run build:prod`  
Runs production build

- `npm run lint`  
Runs eslint javascript linting process

### Child theme
At the moment theme does not have official child theme support. 

### Customization
See our [recipes section](/recipes) to see how to tweak the project to your needs.
