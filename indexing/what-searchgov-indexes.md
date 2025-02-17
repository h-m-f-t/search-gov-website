---
layout: page
title: What Search.gov Indexes From Your Website
crumbname: What Search.gov Indexes
category: admin-center
tags: indexing seo
date: April 24, 2019
last_modified_at: April 24, 2019
sidenav: indexing
redirect_from:
    - /manual/what-searchgov-indexes.md

---

## Content

When we think about indexing pages for search, we usually think about indexing the primary content of the page. But if the page isn’t structured to tell the search engine where that content is to be found, it will collect the `<body>` tag, and then filter out the `<nav>` and `<footer>` elements, if present. If `<main>`, `<nav>`, or `<footer>` are not present, we collect the full contents of the `<body>` tag. Learn more on our post about aiming search engines at the content you really want to be searchable, using [the </main> element]({{ site.baseurl }}/indexing/how-search-engines-index-content-better-discoverability.html#main-element).

## Metadata

You can [read more detail on each of the following elements here]({{ site.baseurl }}/indexing/metadata.html).

### Standard metadata elements

* title
* meta description
* meta keywords
* locale or language (from the opening `<html>` tag)
* url
* lastmod (collected from XML sitemaps)

### [Open Graph protocol](http://ogp.me/)  elements

* og:description
* og:title
* article:published_time
* article:modified_time

## File formats

In addition to HTML pages with their various file extensions, Search.gov indexes the following file types:

* PDFs
* Word docs
* Excel docs
* TXT
* Images can be indexed either using our [Flickr integration]({{ site.baseurl }}/admin-center/content/flickr.html), or by sending us an [MRSS feed]({{ site.baseurl }}/admin-center/content/rss.html). Note that images are not indexed during web page indexing, so you’ll need to use one of these two methods. 

Coming soon:
* Powerpoint

Please note that at this time we cannot index javascript content, [similar to most search engines](https://moz.com/blog/search-engines-ready-for-javascript-crawling). At this time we recommend your team adds well crafted, unique description text for each of your pages, or perhaps auto-generate description tag text from the first few lines of the article text. However the text is added, it should include the keywords you want the page to respond to in search, framed in plain language. This will give us, and other search engines, something to work with when we're matching and ranking results. See our discussion of description [metadata]({{ site.baseurl }}/indexing/metadata.html) for more information.
