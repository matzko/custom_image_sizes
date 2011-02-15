=== Custom Image Sizes ===
Contributors: filosofo
Donate link: http://austinmatzko.com/wordpress-plugins/filosofo-custom-image-sizes/
Tags: image, images, thumbnail, thumbnails, crop, cropping
Requires at least: 2.9
Tested up to: 3.1
Stable tag: 1.0

Custom Image Sizes lets you specify exactly the size in which to display an attachment.

== Description ==
Custom Image Sizes is a WordPress plugin that 

* generates the correctly-sized version of an image's thumbnail, if it doesn't already exist.</li>
* lets you specify custom sizes with a size parameter of <code>'[width]x[height]'</code>.</li>

Read more at the [Custom Image Sizes](http://austinmatzko.com/wordpress-plugins/filosofo-custom-image-sizes/) page.

== Installation ==

1. Upload `filosofo-custom-image-sizes/` to the `/wp-content/plugins/` directory
1. Activate the plugin through the 'Plugins' menu in WordPress

== Usage == 

= The typical WordPress way =

 * Put `add_image_size( 'my_custom_thumbnail_name', 220, 130, true );` in your theme’s functions.php file.
 * Add the code to display that attachment’s thumbnail where you want it to appear: `echo wp_get_attachment_image($attachment_id, 'my_custom_thumbnail_name');`
 * Unlike WordPress by itself, Custom Image Sizes will generate the thumbnail for an image, even if the image was uploaded before this `add_image_size()` was set.

= A more direct Custom Image Sizes way =

 * Call `wp_get_attachment_image_src()` or `wp_get_attachment_image()` with the desired thumbnail `'[width]x[height]'` dimensions, like so:

`
      echo wp_get_attachment_image($attachment_id, '220x80');

      /**
       * The above prints markup like
       * <img width="220" height="80" title="" alt=""
       *    class="attachment-220x80" src="http://www.example.com/path-to-file/something-220x80.jpg" />
       */
`
