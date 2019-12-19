### [GitHub Pages](https://pages.github.com/)

#### Install using Git

If you are a git user, you can install the theme and keep up to date by cloning the repo:

    $ git clone https://github.com/dracula/gh-pages.git

#### Install manually

Download using the [GitHub .zip download](https://github.com/dracula/gh-pages/archive/master.zip) option and unzip them.

#### Activating theme

1.  Add the following to your site's `_config.yml`:  
    
        remote_theme: "dracula/gh-pages"
    
2.  Optionally, if you'd like to preview your site on your computer, add the following to your site's `Gemfile`:  
    
        gem "github-pages", group: :jekyll_plugins
