# Auto Upload External Images

## Description
The **Auto Upload External Images** plugin automatically detects external images in your WordPress post content, uploads them to your media library, and replaces the external URLs with local ones. It also updates Elementor’s data to ensure compatibility with Elementor-built pages, and it clears caches (WP Rocket, Redis, and Elementor) to display the updated URLs on the frontend.

This plugin is ideal for users who want to host images locally for better performance, SEO, and reliability, especially when using Elementor as a page builder.

## Features
- Automatically uploads external images to the WordPress media library.
- Replaces external image URLs in `post_content` with local URLs.
- Updates Elementor’s `_elementor_data` to reflect the new image URLs.
- Clears caches for WP Rocket, Redis, and Elementor to ensure changes are visible.
- Logs all actions for debugging and monitoring.

## Installation
1. Download the plugin folder `auto-upload-images`.
2. Upload the folder to your `/wp-content/plugins/` directory.
3. Activate the plugin through the **Plugins** menu in WordPress.
4. The plugin will automatically run whenever a post is saved or updated.

Alternatively, you can install it by creating a new plugin:
- Create a file named `auto-upload-images.php` in `wp-content/plugins/auto-upload-images/`.
- Copy the plugin code (provided below) into this file.
- Activate the plugin in WordPress.

## Requirements
- WordPress 5.0 or higher.
- PHP 7.4 or higher.
- Elementor (optional, for Elementor compatibility).
- WP Rocket and Redis (optional, for cache clearing).

## Usage
1. Create or edit a post with external image URLs (e.g., `<img src="https://example.com/image.jpg">`).
2. Save the post.
3. The plugin will:
   - Upload the external images to your media library.
   - Replace the URLs in the post content and Elementor data.
   - Clear caches to ensure the new URLs are displayed.

Check the debug log (`wp-content/debug.log`) for detailed logs of the process. Ensure `WP_DEBUG` and `WP_DEBUG_LOG` are enabled in `wp-config.php`:
```php
define('WP_DEBUG', true);
define('WP_DEBUG_LOG', true);
define('WP_DEBUG_DISPLAY', false);
