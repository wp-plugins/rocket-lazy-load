=== Lazy Load Rocket ===
Contributors: wp_media
Tags: lazyload, lazy load, images, thumbnail, thumbnails, smiley, smilies, avatar, gravatar
Requires at least: 2.8.0
Tested up to: 3.8
Stable tag: 1.0

The tiny Lazy Load script for WordPress without jQuery or others libraries.

== Description ==

Lazy Load displays images on a page only when they are visible to the user. This reduces the number of HTTP requests mechanism and improves the loading time.

This plugin works on thumbnails, all images in a post content or in a widget text, avatars and smilies. No JavaScript library such as jQuery is used and the script weighs less than 2kb.

This script is used by WP Rocket plugin cache : http://wp-rocket.me

== Installation ==

1. Upload the complete `rocket-lazy-load` folder to the `/wp-content/plugins/` directory
2. Activate the plugin through the 'Plugins' menu in WordPress

== Frequently Asked Questions ==

= How can deactivate Lazy Load on some pages ? = 

You can use <em>do_rocket_lazyload</em> filter.

Here, an example to put in functions.php files :
`
add_action( 'wp', 'deactivate_rocket_lazyload_on_single' );
function deactivate_rocket_lazyload_on_single() 
{
	
	if( is_single() )
		add_filter( 'do_rocket_lazyload', '__return_false' );
	
}
`

== Changelog ==

= 1.0 =
* Initial release.
