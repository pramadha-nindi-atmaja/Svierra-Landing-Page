# Sierra

Sierra is a responsive WordPress theme for startup and landing-page websites, based on the free [Sierra theme by Colorlib](https://colorlib.com/sierra/). It ships with a customizable one-page front page, blog templates, and Bootstrap-based styling.

![Sierra screenshot](screenshot.png)

## Features

- Customizer-driven front page built from reusable sections:
  slider, about, services, features, build, solutions, skills, progress, portfolio, testimonials, call to action, contact, contact info and Google Map
- Blog templates with post-format support (aside, audio, gallery, image, link, quote, video)
- Bootstrap 4 layout, Font Awesome icons, SCSS sources
- Custom logo, custom header, custom menu (Bootstrap navwalker), footer widget areas
- Sticky posts, featured images, editor styles, RTL support
- Bundled JS plugins: Isotope, Magnific Popup, CounterUp, Circle Progress, jQuery Validate, AJAX Chimp, GMaps

## Requirements

- WordPress 4.7 or later
- PHP 7.0 or later
- Recommended plugin: **Sierra Portfolio** (prompted for installation via TGM Plugin Activation)

## Installation

1. Clone the repository into your WordPress themes directory, including submodules:

   ```bash
   cd wp-content/themes
   git clone --recurse-submodules <repository-url> sierra
   ```

   If you already cloned without submodules:

   ```bash
   git submodule update --init --recursive
   ```

2. In the WordPress admin, go to **Appearance → Themes** and activate **Sierra**.
3. Install the recommended plugin when prompted (**Appearance → Install Plugins**).
4. Create a page using the **Home** template (`page-home.php`) and set it as the static front page under **Settings → Reading**.
5. Customize content under **Appearance → Customize**.

## Project structure

```
sierra/
├── assets/
│   ├── css/            Compiled stylesheets (Bootstrap, Font Awesome, theme styles)
│   ├── scss/           SCSS sources for the theme styles
│   ├── js/             Theme scripts and jQuery plugins
│   ├── vendors/        Third-party JS libraries
│   ├── fonts/          Font Awesome fonts
│   └── img/            Theme images
├── inc/
│   ├── customizer/     Customizer settings
│   ├── libraries/      Git submodules (Epsilon Framework, Epsilon Theme Dashboard)
│   ├── widget/         Widget settings
│   └── ...             Theme classes, helpers, TGMPA config, navwalker
├── template-parts/
│   ├── frontpage/      Front page sections
│   └── content-*.php   Post-format templates
├── functions.php       Theme setup, enqueues and includes
├── style.css           Theme header and base styles
├── page-home.php       Front page template
└── index.php, single.php, page.php, search.php, 404.php, ...
```

## Development

Styles are authored in `assets/scss/` and compiled to `assets/css/style.css`. Compile with any Sass tool, for example:

```bash
sass assets/scss/style.scss assets/css/style.css --watch
```

## License

Released under the [GNU General Public License v2 or later](http://www.gnu.org/licenses/gpl-2.0.html). Original theme by [Colorlib](https://colorlib.com/).
