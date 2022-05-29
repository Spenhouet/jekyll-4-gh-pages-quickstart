---
layout: default
---

# Template for Jekyll 4 with GitHub pages

## Example of extra plugin support

Here an example of the timeago plugin which is not supported when using the out-of-the-box gh-pages plugin.

{% assign date = '2020-04-13T10:20:00Z' %}

- Original date - {{ date }}
- With timeago filter - {{ date | timeago }}

## Example for Sass integration in Jekyll

You have two kinds of Sass files:

1. Main files, which you wish to be output as CSS files
2. Partials, which are used by main files in `@import` statements

Main files are like pages – they go where you want them to be output, and they contain the YAML front matter (`---` lines) at the top. Partials are like hidden Jekyll data, so they go in an underscored directory, which defaults to `_sass`.

You site might look like this:

```
| - _sass
    | - _typography.scss
    | - _layout.scss
    | - _colors.scss
| - assets/css
    | - main.scss
    | - print.scss
```


And so on.

The output, in your `_site` directory, would look like this:

```
| - assets/css
    | - main.css
    | - print.css
```

Boom! Now you have just your SCSS/Sass converted over to CSS with all the proper inputs. See also [assets section in Jekyll's documentation](https://jekyllrb.com/docs/assets/).