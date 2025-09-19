---
title: "New group website launched"
description: "Our first post introducing the group blog."
tags: [website, news]
image: /images/blog/2025-09-12_2.jpg
author: steven-schofield
---

We’re pleased to launch our new group website --- [schofield-lab.github.io](https://schofield-lab.github.io) --- and with it, our group blog! Until now, our pages were hosted within the main UCL website. Ongoing changes to location, styling, and the content management system made it increasingly difficult to keep that site up to date. At the same time, a number of excellent free hosting options for academic websites have become available.  

After looking around, we decided that GitHub Pages would be a good fit, and that the [Lab Website Template](https://github.com/greenelab/lab-website-template) provided an ideal starting point. 

<figure class="blog-image">
  <img src="{{ '/images/blog/2025-09-12_1.jpg' | relative_url }}" alt="The Lab Website template">
  <figcaption>The Lab Website Template</figcaption>
</figure>

The template makes it easy to add our own content without worrying too much about style and layout. Features such as automatic import of citations from the ORCID database are a delight and save a lot of time while simultaneously increasing the visibility of our research. 
<figure class="blog-image">
  <img src="{{ '/images/blog/2025-09-12_2.jpg' | relative_url }}" alt="The new group website">
  <figcaption>The new group website</figcaption>
</figure>

---
For anyone interested in setting up a similar page, the [Lab Website Template](https://greenelab.github.io/lab-website-template/) comes with detailed and extremely helpful instructions and with just some basic knowledge of github functionality these should be enough to get you started. We have some some modifications, including adding `jekyll-seo-tag' search engine optimisation. Some comments on getting that running are below. 

Here’s the minimal, working recipe to add `jekyll-seo-tag` to an LWT site and confirm it’s installed in your Docker container.

###### 1) Add the gem to your Gemfile

```ruby
# Gemfile
gem "jekyll-seo-tag", "~> 2.8"
```

###### 2) Rebuild the Docker image (no cache)

Run this from the **repo root**:

```bash
docker build --no-cache -f .docker/Dockerfile -t lab-website-renderer .
```

##### 3) Sanity check (should print a gem path)

```bash
.docker/run.sh bundle show jekyll-seo-tag
```

###### 4) (Re)launch the site

```bash
./.docker/run.sh
```

###### 5) Enable the plugin in `_config.yml`

Add to your existing `plugins:` list:

```yaml
plugins:
  - jekyll-seo-tag
```

##### 6) Insert the tag in your head include

Add this inside `_includes/head.html`:

```liquid
{% raw %}{% seo %}{% endraw %}
```
