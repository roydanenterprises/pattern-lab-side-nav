# pattern-lab-side-nav
An alternate styleguide navigation for http://patternlab.io

![Pattern Lab Side Nav Example](https://raw.githubusercontent.com/bmuenzenmeyer/pattern-lab-side-nav/master/patternlab-side-nav-example.png)

## Status & Compatibility
This alternate styleguide is still a work in progress.

It works for [Pattern Lab Node](https://github.com/pattern-lab/patternlab-node) and has yet to be tested with [Pattern Lab PHP](https://github.com/pattern-lab/patternlab-php).

## Installation

_Assumes a fresh or stable install of Pattern Lab and all its dependencies._

1. The simplest way to swap out the styleguide navigation is to completely replace the directory. Find the location of your current styleguide code.
  * As of [Pattern Lab Node 1.1.0](https://github.com/pattern-lab/patternlab-node/releases/tag/v1.1.0), this is defaulted to  `./core/styleguide/`, unless you remapped it using the `paths` object inside `./config.json`
 * Prior versions housed `styleguide/` directly in `./public/`
2. Overwrite the `styleguide` directory with the `styleguide/` directory from this repository
3. Find `./source/_patternlab-files/index.mustache` and overwrite it with the contents of `index.mustache` in this repository.
4. Optionally: If you'd like your logo displayed above the navigation like the screenshot shows, do the following:
 * Find `./source/_patternlab-files/partials/patternNav.mustache`
 * Add the following block **after** line 1, just inside `<ol class="sg-nav">`:

     ```html
    <li>
      <img src="https://placeholdit.imgix.net/~text?txtsize=15&txt=logo&w=200&h=40" style="margin: 0 auto; display: block; height: 2em; padding: 5px;" alt="Styleguide logo"/>
    </li>
     ```
 * Add your logo url and style as needed.
 * If you like, move `<li><a href="styleguide/html/styleguide.html" class="sg-pop" data-patternpartial="all">All</a></li>` after your logo entry, or make the logo your link to all patterns.
    * Something like:

      ```html
      <li>
        <a href="styleguide/html/styleguide.html" class="sg-pop" data-patternpartial="all">
          <img src="https://placeholdit.imgix.net/~text?txtsize=15&txt=logo&w=200&h=40" style="margin: 0 auto; display: block; height: 2em;"/>
        </a>
      </li>
      ```
