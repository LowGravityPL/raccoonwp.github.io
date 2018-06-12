---
title: 07. Helpers
permalink: helpers.html
---

RaccoonWP comes with various helpers which aim to help you in development.

#### include_theme_partial
This function is similar to WordPress's `get_template_part` with some crucial difference.

Our function includes theme template partial with the possibility to pass the data from the parent template. 
If template is not present, function will fail silently, displaying error in the debug.log.

Usage in controller file:
```
$data = ['title' => 'Some interesting title'];

include_theme_partial(
    '/partials/layout/page-header.php',
    $data
);
```
Loaded template:
```
<!-- File: /partials/layout/page-header.php -->
<header class="page-header <?= isset($class_name) ? $class_name : ''?>">
    <div class="new-container">
        <h1>
            <?= $title; ?>
        </h1>
    </div>
</header>
```
#### get_entity_list
It is a wrapper function around \WP_Query which makes fetching data easier and more robust. 
It allows for parsing the data via callback function.


### AcfJsonHelper