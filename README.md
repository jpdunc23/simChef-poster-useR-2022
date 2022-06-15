# simChef: an intuitive framework for reliable simulation studies in R

Poster for [useR! 2022](https://user2022.r-project.org/).

- [HTML version](https://jpdunc23.github.io/simChef-poster-useR-2022/poster.html)

## Authors

- James Duncan, UC Berkeley -- Biostatistics
- Tiffany Tang, UC Berkeley -- Statistics
- Corrine F. Elliott, UC Berkeley -- Statistics
- Philippe Boileau, UC Berkeley -- Biostatistics
- Bin Yu, UC Berkeley -- Statistics, EECS, and Biostatistics

## Poster creation

This poster uses a custom [R Markdown](https://rmarkdown.rstudio.com/docs/) HTML
template that integrates the accessible and responsive template from
[cpitclaudel/academic-poster-template](https://github.com/cpitclaudel/academic-poster-template)
with the [Pandoc default HTML5template](https://github.com/jgm/pandoc-templates/blob/master/default.html5).

### Poster blocks

Each "level 1" header tag added to the body of `poster.Rmd` using `#` is
converted to a poster block heading and the content below the `#` until the next
`#` is inserted into the poster block body. For example, `# Example` will create
a poster block with heading "Example" and body from the content below `#
Example`. As this is R Markdown, that content can include code and outputs,
(interactive) plots, LaTeX, etc. If you don't want to include any text in the
heading, just use a `#` followed by no text.

### Custom poster block styling

To add a CSS class for custom styling on a single block, use `{.my-class}` after
the `#` and text, e.g. `# Got Style {.my-style}`.

### Block with empty background

One built-in custom style is an empty background, which is useful for including
stand-alone images that would look awkward with the default poster block
style.

To prevent the poster block styling and instead get a blank background that
still respects the poster layout flow, you can add `{.no-block}` after the `#`
and its text. For example, `# {.no-block}` will create an empty space with no
heading, while `# Empty {.no-block}` will create an empty space with heading
"Empty".

To combine this with a custom style, you can add as many classes as you want
separated by a space: `# Empty {.no-block .my-style}`.

### Rmd to HTML conversion details

To convert from the main markdown content in `poster.Rmd` to the HTML format
needed by `cpitclaudel/academic-poster-template`, there is a small bit of custom
JS in the template which searches for HTML elements with the classes `section`
and `level1`. `rmarkdown`/`pandoc` create these elements when converting
`#` to the corresponding HTML.
