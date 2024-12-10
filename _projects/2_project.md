---
layout: page
title: Personal Website powered by Jekyll
description: Literally this website.
img: assets/img/12.jpg
importance: 1
category: work
related_publications: false
---

**WHAT IS [JEKYLL](https://jekyllrb.com/)?**

Jekyll is a static site generator written in Ruby that converts plain text files (written in Markdown or HTML) into static websites. It is lightweight, fast, and does not require a database, making it an excellent choice for personal blogs, portfolios, and documentation sites. Jekyll is also the engine behind GitHub Pages, allowing seamless integration for free website hosting.

Basically, Jekyll takes your content written in Markdown and generates static HTML pages, which are then served by GitHub Pages. Also, it uses **Liquid**, a powerful templating language, to create dynamic content.


**WHY GITHUB PAGES?**

**Free Hosting:** Host your personal website for free.

**Version Control:** Leverage GitHub's version control system.

**Automated Deployment:** Changes pushed to your repository are automatically reflected on your website.


**TUTORIAL**

First, start by choosing one of the plenty Jekyll themes available, [here](https://jekyllrb.com/docs/themes/).

**Prerequisites:**

Install [Ruby](https://www.ruby-lang.org/en/downloads/).

Install Bundler and Jekyll using:

>gem install bundler

>gem install jekyll

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/jekyll_themes.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Jekyll has endless themes to choose from.
</div>

Now the easiest way to use the theme is to fork the theme's repository and rename it as **your-github-username**.github.io. Or, clone the theme's repository locally and use it as your base project.

Make sure that in this new repository **Settings -> Actions -> General -> Workflow permissions** is set to **Read and write permissions**.

Open file '_config.yml', set url to https://**your-github-username**.github.io and leave baseurl empty (do NOT delete it).

If the theme is available as a Ruby gem, you can install it via your Gemfile:

First create a jekyll site by using:

>jekyll new .

in the github page project directory.

Add the theme gem- gem "jekyll-theme-example", to the 'Gemfile' in your project directory and run:

>bundle install

and update '_config.yml'- theme: jekyll-theme-example, to activate the theme.


