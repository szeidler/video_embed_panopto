REQUIREMENTS
------------

This module requires the following modules:

 * Video Embed Field (https://drupal.org/project/video_embed_field).
 * This module needs 7.x-2.0-beta11 or higher version of Video Embed Field.

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
 * @file
 * Handler info alternation for video_embed_panopto.
 */

/**
 * Implements hook_video_embed_handler_info_alter().
 */
function mymodule_video_embed_handler_info_alter(&$info) {
  $info['panopto']['domains'][] = 'myprefix.cloud.panopto.eu';
}

```
