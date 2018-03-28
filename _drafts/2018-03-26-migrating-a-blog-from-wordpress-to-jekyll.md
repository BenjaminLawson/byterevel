---
title: Migrating a Blog from Wordpress to Jekyll
author: Ben Lawson 
---

After almost 7 years of running Byte Revel with Wordpress on shared hosting, I finally made the leap to migrating the blog to the static site generator Jekyll and free hosting on Github pages. The benefit of this setup is that I can easily write new posts in Markdown, keep the entire website under version control, use the beautiful themes the Jekyll community has made, stop worrying about Wordpress security vulnerabilities, and eliminate my yearly hosting bill. In this post I will outline the steps I took to carry out a successful migration of my Wordpress posts and data to Jekyll and point my domain to GitHub pages.

## 1. Choosing a Theme ##
Jekyll doesn't have nearly as many themes created for it as Wordpress, but the themes that do exist are often high quality and they benefit from the open source culture surrounding them.

## 2. Export Wordpress Content ## 
![Jekyll Exporter]({{ site.url }}/assets/images/jekyll-exporter.png)

Preliminary research revealed two viable tools for exporting Wordpress data to a format Jekyll recognizes: the official "[jekyll-import](https://import.jekyllrb.com/docs/wordpress/)" Ruby gem (recommended in the documentation), and an official Wordpress plugin called "[Jekyll Exporter](https://wordpress.org/plugins/jekyll-exporter/)". The former requires a connection to the database and only exports posts and pages, while the latter promises to export posts, pages, and images with the click of a button. Jekyll Exporter also runs your content through plugin filters that process shortcodes and generate the corresponding HTML. I opted to use Jekyll Exporter, hoping that it would be easier. Unfortunately, I found out that for large websites the plugin runs into resource constraints on shared hosting as of the time of writing, requiring a workaround described in issue [#70](https://github.com/benbalter/wordpress-to-jekyll-exporter/issues/70). Alternatively, you can run your Wordpress website locally and avoid the problem entirely. After extracting the exported files from the plugin, I moved them into my Jekyll website's directory.

## 3. Make a gh-pages Branch ##
It's worth noting that you can choose to have GitHub pages [automatically regenerate your website](https://jekyllrb.com/docs/github-pages/) whenever you push updates to your git repository, but then you are constrained to running "safe" plugins approved by Github and gem-based themes hosted on GitHub. This was a non-option for me as I wanted full control to use custom plugins and easily customize my theme. Fortunately, it's easy to manually generate your website and push to a GitHub pages branch. Here are the commands I used to create a gh-pages branch and checkout the branch in the \_site directory, so that commiting and pushing updates is convenient.

```shell
# make branch an orphan to avoid copying source code
git checkout --orphan gh-pages
git rm -rf .
```

If you really want your website to be automatically generated but don't want the constraints of GitHub Pages, [GitLab](https://about.gitlab.com/2016/04/07/gitlab-pages-setup/) and [Netlify](https://www.netlify.com/blog/2015/10/28/a-step-by-step-guide-jekyll-3.0-on-netlify/) offer free continuous integration services for git repositories that can be configured to build Jekyll websites. I chose to stay on GitHub to keep things simple, and because I trust GitHub to be around longer than any smaller companies.

## 4. Configuring a Domain & Cloudflare ##
