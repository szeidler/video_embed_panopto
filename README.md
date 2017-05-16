REQUIREMENTS
------------

This module requires the following modules:

 * Video Embed Field (https://drupal.org/project/video_embed_field)

INSTALLATION
------------

 * Install as you would normally install a contributed Drupal module. See:
   https://drupal.org/documentation/install/modules-themes/modules-7
   for further information.
 * Implement `hook_video_embed_handler_info_alter()` to whitelist your
   panopto client subdomain.
     * That is required, because panopto does not use an unique host, but
     client-specific subdomains. Otherwise the module will return a
     `This video provider is not currently supported.` validation error.


```php
<?php

/**
 * Implements hook_video_embed_handler_info_alter().
 */
function mymodule_video_embed_handler_info_alter(&$info) {
  $info['panopto']['domains'][] = 'myprefix.cloud.panopto.eu';
}
```