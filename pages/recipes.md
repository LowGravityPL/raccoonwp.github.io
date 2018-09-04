---
title: 06. Recipes
permalink: recipes.html
---

# Recipes
Our main idea was to give you strong, solid structure for your project.
At the same time we want to allow you to add to and shape the project to suit your needs.

Please follow the instructions below to customize Raccoon to your needs.

## Vocabulary

### Running a command
Use your favourite terminal....
[more info needed] 

### Project root
Usually it is...[more info needed]

### Theme directory
The directory your theme files reside in.
By default it is `/public/core/themes/raccoon-theme`

### How to add Custom Post Type or Taxonomy?
Nobody wants to repeat his code. 
That is why we rely on great [Extended CPTs library by John Blackbourn](https://github.com/johnbillion/extended-cpts)

[more info needed]

### How to remove built-in jQuery 
How to remove built-in jQuery 1.x and serve 3.x without breaking the plugins
[more info needed]

### How to add Bootstrap4?
[more info needed]

### How to add Foundation5?
[more info needed]

### How to add Bourbon/Neat?
[more info needed]

### How to add React or Vue?
[more info needed]

### How to disable plugin on certain environment
If you need to disable particular plugin on given environment (for example cache plugin when developing locally)
then all you need to do is:
1. Locate the environment config you want to adjust in the `/RaccoonWP/configuration/` directory.
1. Edit and add following snippet to the file:
    ``` 
    //replace the plugins with the ones which fit your use case
    define('ENV_DISABLED_PLUGINS', [
        'gutenberg/gutenberg.php',
        'autoptimize/autoptimize.php',
    ]);
    ```

If you would like to learn more about the idea and how it works in the background please read
[this article](https://kamilgrzegorczyk.com/2018/05/02/how-to-disable-plugins-on-certain-environment/).

### How to remove support for Twig templates
In case you are not a fan of TWIG templating you should remove Timber plugin from your project.

Run following command in the root of your project:
```
composer remove wpackagist-plugin/timber-library
```

Afterwards navigate to the theme directory and proceed with removal of `Timber::render` function calls as well as all `[filename].twig` templates.

### How to add support for Laravel Blade templates
There are many ways to add a support for Laravel Blade templates.
In our opinion the easiest way to do so is to add [Bladerunner plugin](https://github.com/ekandreas/bladerunner) which will handle it for you.

Run following command in the root of your project:
```
composer require ekandreas/bladerunner
``` 

### How to remove Extended CPTs
If you do not want to use Extended CPTs feature please you should remove the library from your projec dependencies.

Run the following command in the root of your project:
```
composer remove johnbillion/extended-cpts
````

### How to change default wordpress installation path (for upcomming RaccoonWP v1.2.0)
If you'd like to change where wordpress is installed by default you have to change it manually in exactly 5 files. Change these lines in these files to your liking as described below:
- `.env`
  - `WP_SITEURL=${WP_HOME}/wp`
- `RaccoonWP/RaccoonApp.php`
  - `const WP_INSTALL_DIRECTORY_NAME = 'wp';`
- `public/index.php`
  - `require __DIR__ . '/wp/wp-blog-header.php';`
- `composser.json`
  - `"wordpress-install-dir": "public/wp"`
- `.gitignore`
  - `public/wp`