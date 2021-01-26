# Blog

## Why Blogging?

- Store my notes somewhere
- Available everywhere
- May be usefull for others
- Getting rich by affiliate links :D

## Why Github to host the blog?

- Free
- Most open-source software are hosted here
- Simple
- Available everywhere

## Jekyll or Eleventy?

### Why Jekyll?

- Simple
- Markdown

### Why not Jekyll?

- I don't want the Ruby stack on my machine (gem bundler)

### Why Eleventy (11ty)?

- Eleventy looks cooler, although it seems harder (no out of the box layout for example)
- This forces me to look into CSS - my not so favorite language...
- Out-of-the-box support for many templating engines: <https://www.11ty.dev/docs/languages/>
  - MarkDown
  - Nunjucks
  - Liquid
  - Handlebars
  - Mustache
  - ...
  
### Why not Eleventy (11ty)?

- no out of the box layout

## Jekyll

### Install Jekyll

- Windows: <https://jekyllrb.com/docs/installation/windows/>
  - January 2021: WSL2 did not work for me (installation was fine, but Jekyll did not start
- Others: <https://jekyllrb.com/docs/installation/>

### Use Jekyll

Create a new github repository using this naming convention: `<your-github-name>.github.io`. Check this out locally:

Open this new folder in cmd, reate new Blog: `jekyll new . --force` (force is needed, because the folder is not empty. ".git" is already there)

Open cmd in your blog, enter `jekyll s`

Install file watcher: `gem install jekyll-watch`

Open cmd in your blog, enter `jekyll s --watch`

### Config for Github

Check the `Gemfile` readme's.

### Fixing äöü issue

Add `encoding: utf-8` to your `_config.yml` file

### Links

- Jekyll: <https://jekyllrb.com/>
- Jekyll Dark Theme: <https://blog.slowb.ro/dark-theme-for-minima-jekyll/>

## Eleventy

Install Eleventy: <https://www.11ty.dev/>. 

Create your first blog: Open a new folder and run:

```bash
npm init -y
npm install --save-dev @11ty/eleventy
```

In this folder, create 2 files: 

a) index.html

```html
<!doctype html>
<html>
  <head>
    <title>Page title</title>
  </head>
  <body><p>Hi</p>
  </body>
</html>
```

b) README.md

```bash
# Page header
```

Run it:

```bash
npx @11ty/eleventy --serve
```

As you can see in the Output, you can run your site right away: `http://localhost:8080`

```bash
c:\Work.proj\blog_>npx @11ty/eleventy --serve
Writing _site/index.html from ./index.html.
Writing _site/README/index.html from ./README.md.
Wrote 2 files in 0.10 seconds (v0.11.1)
Watching…
[Browsersync] Access URLs:
 ------------------------------------
       Local: http://localhost:8080
    External: http://172.19.80.1:8080
 ------------------------------------
          UI: http://localhost:3001
 UI External: http://localhost:3001
 ------------------------------------
[Browsersync] Serving files from: _site
```
