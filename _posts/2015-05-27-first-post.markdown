---
layout: post
comments: true
title:  "My first post using jekyll on github"
excerpt: "Build a blog on github, use the jekyll and disqus."
date:   2015-05-27 15:00:00
mathjax: true
---


I build my blog on [Github](https://github.com/zlmzju/blog) by following [this page](https://help.github.com/articles/using-jekyll-with-pages/).

## Jekyll: static site generator

### What is Jekyll
> Jekyll is a site generator.

If we want to build a blog website, we need to do a lot of extra things in addition to
writing a blog post, such as writing the `index.html`, post link list, and some 
`html`, `CSS`, or `JavaScript` language.

Jekyll can help you handle all these staffs, and you can focus on writing. 
Instead of writing `html`, you will use a much simpler language `Markdown` to write a blog post.
After that, Jekyll will convert the post to static pages, i.e. `html` file. 
In the meantime, the whole site will be built with a beatiful page style and organization.

So Jekyll is just a software for converting your posts to a sit. Some other similar softwares are also 
popular, such as `Hexo`, `FarBox` and `Octopress`.
Some guys say that `Hexo` is much efficient than `Jekyll` and its themes are more beautiful.
But I got stuck using `Hexo` with one by one little problems. So I think `Jekyll` is more stable and it is
the official tool suggested by `Github`.

### How to install Jekyll
Jekyll is written in `Ruby`, so we will install `Ruby` and install `Jekyll` from Ruby package host `RubyGems`.

```shell
sudo apt-get install ruby2.0 ruby2.0-dev #Jekyll dependencies, you can install them in other way.
```

Then install `Jekyll` when you have got `Ruby` in your system.

```shell
sudo gem install jekyll
```

So easy!

### How to use Jekyll

**Init**. Now you can build a new blog site with Jekyll.

```shell
jekyll new myblog
```

Then you will see a new directory named `myblog`.
Change your directory to `myblog` and type:
```shell
jekyll serve
```

Now browse to `http://localhost:4000` and you can see a new blog website.

**Write**. Now you can write your own blog post.

Create a markdown file in the `_posts` directory with a name like `YEAR-MONTH-DAY-title.markdown`.
When you finished the post writing, then convert the post to `html` by

```shell
jekyll build
```

Then you will see your post in the website `http://localhost:4000`.

Other usages please checkout [the official document](http://jekyllrb.com/docs/home/).


## GitHub Pages: host your site
>Hosted directly from your GitHub repository. Just edit, push, and your changes are live.

### Create a repository
Create a repository in GitHub, such as `blog`.
Github will automatically convert the `gh-pages` branch in your repo to a website by using their `Jekyll`.

### Push your repo to GitHub
So we can push our contents to the `gh-pages` branch of GitHub repo.

In your local machine and the `myblog` directory, init local repo and commit.

```shell
git init
git remote add origin https://github.com/yourusername/yourrepo.git
git checkout -b gh-pages
```
When you have finished and tested your blog posts, you can push them to GitHub.

```shell
git push origin gh-pages
```

Now your website will be available for your own url (see Jekyll docs for url configuration).

###End
All suggestions are welcome.



