# Starter
Starter kit for emulsify for Drupal. This is a base emulsify setup for multiple project. 

# How to setup
## Requisites
Unified twig extension: https://packagist.org/packages/drupal-pattern-lab/unified-twig-extensions
Components library: https://www.drupal.org/project/components 

# Steps
1. Clone the repo into `/themes/custom`
2. Rename `starter`for the name desired in all files.
3. Run `npm install` on the root of the theme. It's possible some permission errors pop up if you are using docker. You will have to run the bash scripts manually: `bash scripts/pattern_lab.sh` and then `bash scripts/twig_functions.php`. Those scripts will download patter-lab folder and twig functions.
4. Enable the theme and also the requiered modules: `drush then THEME_NAME -y && drush en components unified_twig_ext -y`
5. Setup the `local.gulp-config.js` on the root of the theme. Recommended to use this setup: https://github.com/fourkitchens/emulsify-gulp/blob/develop/gulp-config.js
6. Run `npm start`


Original documentation by Four Kitchens (Emulsify):

[![Four Kitchens](https://img.shields.io/badge/4K-Four%20Kitchens-35AA4E.svg)](https://fourkitchens.com/)

# starter: Pattern Lab + Drupal 8

Component-driven prototyping tool using [Pattern Lab v2](http://patternlab.io/) automated via Gulp/NPM. Also serves as _a starterkit_ Drupal 8 theme.

## Requirements

1.  [PHP 7.1](http://www.php.net/)
2.  [Node (we recommend NVM)](https://github.com/creationix/nvm)
3.  [Gulp](http://gulpjs.com/)
4.  [Composer](https://getcomposer.org/)
5.  Optional: [Yarn](https://github.com/yarnpkg/yarn)

## Prototyping (separate from Drupal, Wordpress, etc.)

starter supports both NPM and YARN.

Install with NPM:
`composer create-project fourkitchens/starter:^3.0 --stability dev --no-interaction starter && cd starter && npm install`

Install with Yarn:
`composer create-project fourkitchens/starter:^3.0 --stability dev --no-interaction starter && cd starter && yarn install`

## Drupal installation

### In a Composer-based Drupal install (recommended)

1. Require starter in your project `composer require fourkitchens/starter`
2. Move into the original starter theme `cd web/themes/contrib/starter/`
3. Create your new theme by cloning starter `php starter.php "THEME NAME"` (Run `php starter.php -h` for other available options)
4. Move into your theme directory `cd web/themes/custom/THEME_NAME/`
5. Install the theme dependencies `npm install` or `yarn install`
6. Enable your theme and its dependencies `drush then THEME_NAME -y && drush en components unified_twig_ext -y`
7. Proceed to the "Starting Pattern Lab…" section below

If you're not using a Composer-based Drupal install (e.g. tarball download from drupal.org) installation [instructions can be found on the Wiki](https://github.com/fourkitchens/starter/wiki/Installation).

Troubleshooting Installation: See [Drupal Installation FAQ](https://github.com/fourkitchens/starter/wiki/Installation#drupal-installation-faq).

_Note: Once you've created your custom theme, you can remove starter as a dependency of your project. If you'd like to get updates as we push them, solely for educational/best-practice information, feel free to leave it in and receive the updates. Updating starter will not affect your custom theme in any way._

## Starting Pattern Lab and watch task

The `start` command spins up a local server, compiles everything (runs all required gulp tasks), and watches for changes.

1.  `npm start` or `yarn start`

---

## Highlighted Features

<table><tbody>
<tr><td>Lightweight</td><td>✔</td><td>starter is focused on being as lightweight as possible.</td></tr>
<tr><td>SVG sprite support </td><td><strong>✔</strong></td><td>Automated support for creating SVG sprites mixins/classes.</td></tr>
<tr><td>Stock Drupal templates </td><td><strong>✔</strong></td><td>Templates from Stable theme - see /templates directory</td></tr>
<tr><td>Stock Components </td><td><strong>✔</strong></td><td>with Drupal support built-in (https://github.com/fourkitchens/starter#starters-built-in-components-with-drupal-support)</td></tr>
<tr><td>Performance Testing </td><td><strong>✔</strong></td><td>Support for testing via Google PageSpeed Insights and WebPageTest.org (https://github.com/fourkitchens/starter/wiki/Gulp-Config#performance-testing)</td></tr>
<tr><td>Automated Github Deployment </td><td><strong>✔</strong></td><td>Deploy your Pattern Lab instance as a Github page (https://github.com/fourkitchens/starter/wiki/Gulp-Config#deployment)</td></tr>
</tbody></table>

<h3 id="components">starter's Built in Components with Drupal support</h3>
Forms, tables, video, accordion, cards, breadcrumbs, tabs, pager, status messages, grid

View a [demo of these default starter components](https://fourkitchens.github.io/starter/pattern-lab/public/).

## Documentation

Documentation is currently provided in [the Wiki](https://github.com/fourkitchens/starter/wiki). Here are a few basic links:

#### General Orientation

See [Orientation](https://github.com/fourkitchens/starter/wiki/Orientation)

We have a [series of videos](https://www.youtube.com/playlist?list=PLO9S6JjNqWsGMQLDfE8Ekt0ryrGa3g4km) for you to learn more about starter.

#### For Designers (Prototyping)

See [Designers](https://github.com/fourkitchens/starter/wiki/For-Designers)

#### For Drupal 8 Developers

See [Drupal Usage](https://github.com/fourkitchens/starter/wiki/Drupal-Usage)

#### Gulp Configuration

See [Gulp Config](https://github.com/fourkitchens/starter/wiki/Gulp-Config)
