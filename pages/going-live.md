---
title: 07. Going live?
permalink: going-live.html
---

# Going live ideas?
1. Consider adding `"optimize-autoloader": true` to your composer.json config.
1. Do NOT deploy/upload following files/directories:
    - Composer configuration - `composer.json`, `composer.lock`,
    - theme `package.json`
    - theme `node_modules`
    - non-compiled theme assets (use `dist/` on production)
    - theme webpack configuration (`build-util` directory)
    - and other files like `.eslintrc.js`, `README>md` and many more.
     
1.  Consider adding "production" plugins like:
    - Minification plugin (i.e. [autoptimize](https://wordpress.org/plugins/autoptimize/)).
    - Caching plugin (i.e. [WP Super Cache](https://wordpress.org/plugins/wp-super-cache/)).
    - Image optimization plugin (i.e. [Shortpixel](https://wordpress.org/plugins/shortpixel-image-optimiser)).
    
    Before adding ANY performance related plugins measure your performance first! 
1. Focus on your web server configuration. Make sure you use reliable and performant service. 
Use performance and availability monitoring. 
1. Do not forget about backup policy. Better to be safe than sorry  