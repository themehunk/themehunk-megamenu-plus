# Plugin Structure: Easy Mega Menu Plus

**Plugin Name:** Easy Mega Menu Plus
**Version:** 1.1.2
**Author:** Themehunk
**Text Domain:** `themehunk-megamenu`

---

## Directory Structure

```
themehunk-megamenu-plus/
│
├── themehunk-megamenu.php          # Main plugin entry point — defines constants, includes all files
│
├── inc/                            # Core PHP includes
│   ├── megamenu-base.php           # Base setup and initialization
│   ├── megamenu-class.php          # Main plugin class
│   ├── megamenu-default-option.php # Default option values
│   ├── megamenu-functions.php      # Helper/utility functions
│   ├── megamenu-nav-menu-metadata.php  # Nav menu item metadata handling
│   ├── megamenu-nav-menu-settings.php  # Nav menu settings panel
│   ├── megamenu-setting.php        # Plugin settings page
│   ├── megamenu-style.php          # Dynamic inline style generation
│   ├── megamenu-widgets.php        # Widget integration
│   ├── toggle-themehunk-megamenu.php   # Enable/disable megamenu toggle logic
│   └── walker.php                  # Custom Walker class for nav menu output
│
├── views/
│   └── admin/
│       └── item_settings.php       # Admin UI for individual menu item settings
│
├── assets/
│   ├── css/
│   │   ├── megamenu.css            # Frontend styles
│   │   └── megamenu-admin.css      # Admin panel styles
│   ├── js/
│   │   ├── megamenu.js             # Frontend JavaScript
│   │   ├── megamenu-admin.js       # Admin panel JavaScript
│   │   └── settings.js             # Settings page JavaScript
│   └── images/
│       ├── center-align.png
│       ├── left-align.png
│       ├── right-align.png
│       ├── panel-left.png
│       ├── panel-right.png
│       └── loading.gif
│
├── lib/                            # Third-party libraries
│   ├── codemirror/
│   │   ├── codemirror.css
│   │   └── codemirror.js           # Code editor (custom CSS input)
│   ├── font-awesome-4.7.0/
│   │   ├── css/
│   │   │   ├── font-awesome.css
│   │   │   └── font-awesome.min.css
│   │   └── fonts/                  # FontAwesome webfont files
│   ├── pickr/
│   │   ├── css/
│   │   │   ├── classic.min.css
│   │   │   ├── monolith.min.css
│   │   │   └── nano.min.css
│   │   └── js/
│   │       └── pickr.min.js        # Color picker library
│   ├── select/
│   │   ├── select.css
│   │   └── select.min.js           # Custom select/dropdown library
│   ├── spectrum/
│   │   ├── spectrum.css
│   │   └── spectrum.js             # Spectrum color picker
│   └── wpcolorpicker-alpha.js      # WP color picker with alpha support
│
├── notify/                         # Admin notification/promo system
│   ├── notify.php                  # Notification loader (conditionally included)
│   ├── notify-html.php             # Notification HTML template
│   └── assets/
│       ├── css/
│       │   ├── notice.css
│       │   └── owl.carousel.css
│       ├── js/
│       │   ├── themehunk-notify.js
│       │   └── owl.carousel.js
│       └── images/
│           ├── m-shop.png
│           └── royal-shop.png
│
└── readme.txt                      # WordPress.org readme
```

---

## Key Constants

| Constant | Value |
|---|---|
| `THEMEHUNK_MEGAMENU_VERSION` | `1.1.2` |
| `THEMEHUNK_MEGAMENU_URL` | Plugin directory URL |
| `THEMEHUNK_MEGAMENU_DIR` | Plugin directory path |

---

## Load Order (main plugin file)

1. `inc/megamenu-setting.php`
2. `inc/megamenu-default-option.php`
3. `inc/megamenu-base.php`
4. `inc/megamenu-class.php`
5. `inc/toggle-themehunk-megamenu.php`
6. `inc/megamenu-functions.php`
7. `inc/megamenu-nav-menu-settings.php`
8. `inc/megamenu-widgets.php`
9. `inc/walker.php`
10. `inc/megamenu-style.php`
11. `notify/notify.php` *(conditionally — only if no other Themehunk plugins are active)*
