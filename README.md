# zola-tailwindcss

This project is a GitHub template for creating web projects that use the [Zola](https://getzola.org) static site generator, in conjunction with [Tailwindcss](https://tailwindcss.com). It currently works for zola `v0.19.x` and tailwind `v3.4.x`.

## Installation

Run `npm install` to download the tailwind dependencies. The project is now ready to be used.

## Usage

Here's how you do stuff:

```zsh
# installs everything
# that you need
npm install

# build builds once,
# output in `./public`
npm run build

# starts a local server
# that watches/rebuilds
npm run serve

## Use can also use `BUILD_OPTS` or `SERVE_OPTS`
## To specifiy options for those commands, e.g.
BUILTS_OPTS="--drafts" npm run build
SERVE_OPTS="--port 1234" npm run serve
```

For example, you can run `npm run serve` and then go to `localhost:1111` in your browser to see the websites. As you make changes to the code or content, the website will be updated.

## Content

Content is stored in [markdown text](https://commonmark.org/help/) files located within the `content` directory. Files named `_index.md` are called "sections", and files by any other name ending in `.md` are called "pages". For more information you can read the [zola](https://www.getzola.org/documentation/content/overview/) documentation. The markdown is inserted into the html via the specified "[template](#templates)", which is indicated at the top of the content's "front matter".

## Templating

Templates are html files stored in the `templates` directory. Their purpose is to decide where in the html the content goes. The content is accessible to the template as a variable named either `section.content` or `page.content`, depending on the context. Within the template file, you can use a templating language called [tera](http://tera.netlify.app/docs/). There are examples throughout this document of templating, wherever you see the `{{ template_variable }}`.

## Styling

This website uses [tailwindcss](https://tailwindcss.com/) for most of its styling. Separate CSS can be added either in the `sass` directory or in static for just plain css. Since Tailwind 4.x.y, configuration happens now in `input.css` instead of tailwind.config.css.

## Dependencies and Tools

* [zola](https://getzola.org) `brew install zola`
* node, npm

## Notes:

* The `npm run serve` script runs two long-running tasks in parallel and allows both to write simultaneously to STDOUT by using [a mixture of `wait` and sending jobs to the background](https://www.cyberciti.biz/faq/how-to-run-command-or-code-in-parallel-in-bash-shell-under-linux-or-unix/)
