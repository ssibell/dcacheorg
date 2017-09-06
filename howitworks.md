---
layout: page
title: Getting Started
permalink: /getting-started/
top_graphic: 3
redirect_from: "/howitworks"
---
# Welcome
This aim of this tutorial is to be a comprehensive guide to this website. We’ll cover topics such as getting your site up and running, creating and managing your content like posts, downloads, documentations and many more. And customizing the way this site works and looks, deploying to various environments, and give you some advice on participating in the future development of Jekyll itself.

# So what is Jekyll?

Jekyll is a simple, blog-aware, static site generator. It takes a template directory containing raw text files in various formats, runs it through a converter (like Markdown) and our Liquid renderer, and spits out a complete, ready-to-publish static website suitable for serving with your favorite web server. Jekyll also happens to be the engine behind GitHub Pages, which means you can use Jekyll to host your project’s page, blog, or website from GitHub’s servers for free.

## How does Jekyll work?
Jekyll can be confusing at first. Jekyll actually only does one of a few things to your files, although it classifies files in many different ways.
Jekyll either copies, omits or transforms files from your source directory into an output directory.

1 When Jekyll transforms your file, it will always be in the following way, potentially skipping steps.
2 If a file begins with yaml frontmatter, Jekyll will apply the following transformation to that file:

liquid templating: liquid template parsing is run on the original content of the file, with several variables, like site or page provided as arguments your liquid templates can access.
converting the content: Jekyll asks converters whether they match your file’s extension, e.g. kramdown matches .md, and if so they run against the output from template parsing. Different converters run depending on your file’s extension, e.g. .md extension and the kramdown converter.
layout parsing: The output of conversion is passed as the  ```{{content}}``` variable to either your default layout, or the layout specified in your file’s yaml frontmatter.
The output of the layout is written to a file in your output directory, or omitted.
Now I want to walk through an example of Jekyll applying this transformation. Later in Jekyll’s core and Testing a complete build we will look at the general structure Jekyll’s algorithm follows and what sorts of files get which treatment.

# How can I create a new post? 

We will create a post in the `_posts` folder. As we can see, there are 3 folders in `_posts` folder. 

If we create a new file in any of the folders, which are categories, with required lines, will published in the main page. 
