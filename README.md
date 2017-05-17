REQUIREMENTS
------------

This module requires the following modules:

 * Video Embed Field (https://drupal.org/project/video_embed_field)

INSTALLATION
------------

 * Install as you would normally install a contributed Drupal module. See:
   https://drupal.org/documentation/install/modules-themes/modules-7
   for further information.
   
CONFIGURATION
------------

 * Open the Video Embed Field configuration page at
   `admin/config/media/vef/settings` and specify your client domains.


Alternatively you can programatically specify your client domains
implementing `hook_video_embed_handler_info_alter()`.

```php
<?php

/**
 * Implements hook_video_embed_handler_info_alter().
 */
function mymodule_video_embed_handler_info_alter(&$info) {
  $info['panopto']['domains'][] = 'myprefix.cloud.panopto.eu';
}
```