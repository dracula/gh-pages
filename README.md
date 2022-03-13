# Dracula for [GitHub Pages](https://pages.github.com/)

[![Build Status](https://travis-ci.org/dracula/gh-pages.svg?branch=master)](https://travis-ci.org/dracula/gh-pages)

> A dark theme for [GitHub Pages](https://pages.github.com/), full preview at [preview the theme to see what it looks like](http://dracula.github.io/gh-pages/).

![Screenshot](./screenshot.png)

## Install

All instructions can be found at [draculatheme.com/github-pages](https://draculatheme.com/github-pages).

## Customizing

#### Configuration variables

Dracula will respect the following variables, if set in your site's `_config.yml`:

```yml
title: [The title of your site]
description: [A short description of your site's purpose]
```

Additionally, you may choose to set the following optional variables:

```yml
show_downloads: ["true" or "false" to indicate whether to provide a download URL]
google_analytics: [Your Google Analytics tracking ID]
show_header: ["true" or "false" to indicate whether to show the top header]
```

There are also currently the following optional page variables:

```yml
icon: [path to file including extension]
colorspace: [primary page color cyan/green/orange/pink/purple/red/yellow]
```

#### Stylesheet

If you'd like to add your own custom styles:

1. Create a file called `/assets/css/style.scss` in your site
2. Add the following content to the top of the file, exactly as shown:

   ```scss
   ---
   ---

   @import "{{ site.theme }}";
   ```

3. Add any custom CSS (or Sass, including imports) you'd like immediately after the `@import` line

_Note: If you'd like to change the theme's Sass variables, you must set new values before the `@import` line in your stylesheet._

#### Layouts

If you'd like to change the theme's HTML layout:

1. [Copy the original template](https://github.com/dracula/gh-pages/blob/master/_layouts/default.html) from the theme's repository<br />(_Pro-tip: click "raw" to make copying easier_)
2. Create a file called `/_layouts/default.html` in your site
3. Paste the default layout content copied in the first step
4. Customize the layout as you'd like

#### Overriding GitHub-generated URLs

Templates often rely on URLs supplied by GitHub such as links to your repository or links to download your project. If you'd like to override one or more default URLs:

1. Look at [the template source](https://github.com/dracula/gh-pages/blob/master/_layouts/default.html) to determine the name of the variable. It will be in the form of `{{ site.github.zip_url }}`.
2. Specify the URL that you'd like the template to use in your site's `_config.yml`. For example, if the variable was `site.github.url`, you'd add the following:
   ```yml
   github:
     zip_url: http://example.com/download.zip
     another_url: another value
   ```
3. When your site is built, Jekyll will use the URL you specified, rather than the default one provided by GitHub.

_Note: You must remove the `site.` prefix, and each variable name (after the `github.`) should be indent with two space below `github:`._

For more information, see [the Jekyll variables documentation](https://jekyllrb.com/docs/variables/).

#### Previewing the theme locally

If you'd like to preview the theme locally (for example, in the process of proposing a change):

1. Clone down the theme's repository (`git clone https://github.com/dracula/gh-pages`)
2. `cd` into the theme's directory
3. Run `script/bootstrap` to install the necessary dependencies
4. Run `bundle exec jekyll serve` to start the preview server
5. Visit [`localhost:4000`](http://localhost:4000) in your browser to preview the theme

#### Running tests

The theme contains a minimal test suite, to ensure a site with the theme would build successfully. To run the tests, simply run `script/cibuild`. You'll need to run `script/bootstrap` one before the test script will work.

## Team

This theme is maintained by the following person(s) and a bunch of [awesome contributors](https://github.com/dracula/gh-pages/graphs/contributors).

| [![backlands](https://avatars1.githubusercontent.com/u/12586299?v=3&s=70)](https://github.com/backlands) |
| -------------------------------------------------------------------------------------------------------- |
| [backlands](https://github.com/backlands)                                                                |

## Community

- [Twitter](https://twitter.com/draculatheme) - Best for getting updates about themes and new stuff.
- [GitHub](https://github.com/dracula/dracula-theme/discussions) - Best for asking questions and discussing issues.
- [Discord](https://draculatheme.com/discord-invite) - Best for hanging out with the community.

## License

[MIT License](./LICENSE)
