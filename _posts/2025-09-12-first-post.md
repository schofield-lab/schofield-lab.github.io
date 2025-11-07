---
title: "New group website launched"
description: "Our first post introducing the group blog."
tags: [website, news]
image: /images/blog/2025/2025-09-12_2.jpg
author: steven-schofield
---

We’re pleased to launch our new group website — [schofield-lab.github.io](https://schofield-lab.github.io) — and with it, our group blog!  

Until now, our pages were hosted within the main UCL website. Ongoing changes to location, styling, and the content management system made it increasingly difficult to keep that site up to date. At the same time, a number of excellent free hosting options for academic websites have become available.  

After looking around, we decided that GitHub Pages would be a good fit, and that the [Lab Website Template](https://github.com/greenelab/lab-website-template) provided an ideal starting point.  

<figure class="blog-image">
  <img src="{{ '/images/blog/2025/2025-09-12_1.jpg' | relative_url }}" alt="The Lab Website template">
  <figcaption>The Lab Website Template</figcaption>
</figure>

The template makes it easy to add our own content without worrying too much about style and layout. Features such as automatic import of citations from the ORCID database are a delight — saving time while increasing the visibility of our research.  

<figure class="blog-image">
  <img src="{{ '/images/blog/2025/2025-09-12_2.jpg' | relative_url }}" alt="The new group website">
  <figcaption>The new group website</figcaption>
</figure>

---

### Customisations

For anyone interested in setting up a similar page, the [Lab Website Template](https://greenelab.github.io/lab-website-template/) comes with detailed instructions. With basic GitHub and Markdown/HTML knowledge, plus Docker if you want to run the site locally, it should be enough to get you started, and the final result is an attractive and easy to maintain and update website.

Having said that, we have made a few modifications to suit our needs:  

- **Search engine optimisation** — added jekyll-seo-tag.
- **Cookie management** — included a lightweight JavaScript banner that asks visitors to accept cookies and remembers their choice.  
- **Mobile styling** — tweaked the CSS so the site looks cleaner on phones and tablets. Images resize automatically, text has more breathing space, and the navigation menu stacks neatly on smaller screens.  

---

### Adding jekyll-seo-tag

Here’s the minimal working recipe to add [`jekyll-seo-tag`](https://github.com/jekyll/jekyll-seo-tag) in your Docker container:

1. Add the gem to your Gemfile:

   ```ruby
   gem "jekyll-seo-tag", "~> 2.8"
````

2. Rebuild the Docker image (no cache):

   ```bash
   docker build --no-cache -f .docker/Dockerfile -t lab-website-renderer .
   ```

3. Sanity check (should print a gem path):

   ```bash
   .docker/run.sh bundle show jekyll-seo-tag
   ```

4. (Re)launch the site:

   ```bash
   ./.docker/run.sh
   ```

5. Enable the plugin in `_config.yml`:

   ```yaml
   plugins:
     - jekyll-seo-tag
   ```

6. Insert the tag in your head include:

   ```liquid
   {% raw %}{% seo %}{% endraw %}
   ```

7. You will also then want to tidy up by removing the hard-coded SEO information in `_includes/meta.html`.

---

### Adding a Cookie Banner

To handle cookies, we used the open-source [CookieConsent](https://github.com/osano/cookieconsent) library (via CDN) together with a small amount of custom JavaScript. This allows us to run in opt-in mode, defer embedded content such as YouTube or Google Maps until consent is given, and give visitors the option to revoke or reopen settings at any time.  

---

### Mobile Styling Tweaks

A couple of CSS adjustments helped make the site look better on phones and tablets. Add these rules to your main stylesheet, or create a new `mobile.scss` under `_styles/`

```css

/* Add breathing room for text on small screens */
body {
  padding-left: 0.75rem;
  padding-right: 0.75rem;
}
@media (min-width: 1025px) {
  body {
    padding-left: 0;
    padding-right: 0;
  }
}

@media (max-width: 768px) {
  .navbar,
  .site-nav,
  nav[role="navigation"] {
    position: static !important;
    top: auto !important;
  }

  header,
  .site-header,
  .header {
    position: relative !important;          /* anchor ::before overlay */
    overflow: hidden !important;            /* clip bg/overlay to header */
    background-attachment: scroll !important; /* prevent parallax bleed */
  }

  header::before,
  .site-header::before,
  .header::before {
    position: absolute !important;
    inset: 0 !important;                    /* top/right/bottom/left: 0 */
  }

```
