---
title: Going live?
permalink: going-live.html
---

# Going live ideas?
1. Consider adding `"optimize-autoloader": true` to your composer.json config.
1. Do not upload core files to production environment like:
    - Composer configuration
    - package.json
    - node_modules
    - non-compiled assets
    - webpack configuration
    - and other
    
    More exhaustive list of files that you SHOULD NOT upload to production [link here] 
1.  Consider adding "production" plugins like:
    - minification plugin (i.e. [autoptimize](https://wordpress.org/plugins/autoptimize/)) 
    - caching plugin (i.e. [WP Super Cache](https://wordpress.org/plugins/wp-super-cache/))
    - image optimization plugin (i.e. [Shortpixel](https://wordpress.org/plugins/shortpixel-image-optimiser))
    
    Before adding ANY performance related plugins measure your performance first! 
1. Focus on your web server configuration. Make sure you use reliable and performant service. 
Use performance and availability monitoring. 
1. Do not forget about backup policy. Better to be safe than sorry  