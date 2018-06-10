---
title: 06. Going live?
permalink: going-live.html
---

# Going live ideas?
1. Consider adding `"optimize-autoloader": true` to your composer.json config.
1. Do not deploy/upload following files:
    - Composer configuration - `composer.json`, `composer.lock`,
    - package.json
    - node_modules
    - non-compiled assets (use dist/ on production)
    - webpack configuration
    - and other
     
1.  Consider adding "production" plugins like:
    - Minification plugin (i.e. [autoptimize](https://wordpress.org/plugins/autoptimize/)).
    - Caching plugin (i.e. [WP Super Cache](https://wordpress.org/plugins/wp-super-cache/)).
    - Image optimization plugin (i.e. [Shortpixel](https://wordpress.org/plugins/shortpixel-image-optimiser)).
    
    Before adding ANY performance related plugins measure your performance first! 
1. Focus on your web server configuration. Make sure you use reliable and performant service. 
Use performance and availability monitoring. 
1. Do not forget about backup policy. Better to be safe than sorry  