---
layout: page
title: Metadata and tags you should include in your website
crumbname: Metadata
category: admin-center
redirect_from: 
  - /blog/metadata.html
  - /manual/metadata.html
tags: indexing seo
date: September 1, 2020
last_modified_at: September 1, 2020
sidenav: indexing
---

Search.gov, like other search engines, relies on structured data to help inform how we index your content and how it is presented in search results. You should also read up on the metadata and structured data used by [Google](https://support.google.com/webmasters/answer/79812?hl=en) and [Bing](https://www.bing.com/webmaster/help/marking-up-your-site-with-structured-data-3a93e731).

Including the following tags and metadata in each of your pages will improve the quality of your content's indexing, as well as results ranking. We also encourage you to read about more [HTML5 semantic markup](https://www.semrush.com/blog/semantic-html5-guide/) you can include in your websites.

This page will be updated over time as we add more tag-based indexing functions and ranking factors to our service.

`<title>`
<br>**Detail:** Unique title of the page. If you want to include the agency or section name, place that after the actual page title.
<br>**Used in:** Query matching, term frequency scoring<br>
<br>
`<meta name="description" content="foo" />` 
<br>**Detail:** Your well crafted, plain language summary of the page content. This will often be used by search engines in place of a page snippet. Be sure to include the keywords you want the page to rank well for. Best to limit to 160 characters, so it will not be truncated. [Read more here](https://moz.com/learn/seo/meta-description).
<br>**Used in:** Query matching, term frequency scoring<br>
<br>
`<meta name="keywords" content="foo bar baz" />`
<br>**Detail:** While not often used by commercial search engines due to [keyword stuffing](https://support.google.com/webmasters/answer/66358?hl=en), Search.gov indexes your keywords, if you have added them.
<br>**Used in:** Query matching, term frequency scoring<br>
<br>
`<meta property="og:title" content="Title goes here" />`
<br>**Detail:** Usually duplicative of `<title>`, we use the `og:title` property as the result title if it appears to be more substantive than the `<title>` tag. Note, Open Graph elements are used to display previews of your content in FaceBook and some other social media platforms.
<br>**Used in:** Query matching, term frequency scoring<br>
<br>
`<meta property="og:description" content="Description goes here" />`
<br>**Detail:** Often duplicative of the meta description, we index this field as well, in case it has different content. This field is a good opportunity to include more keywords than you could write into the meta description. Note, Open Graph elements are used to display previews of your content in FaceBook and some other social media platforms.
<br>**Used in:** Query matching, term frequency scoring<br>
<br>
`<meta property="article:published_time" content="YYYY-MM-DD" />`
<br>**Detail:** Exact time is optional; [read more here](https://en.wikipedia.org/wiki/ISO_8601).
<br>**Used in:** Page freshness scoring.<br>
<br>
`<meta property="article:modified_time" content="YYYY-MM-DD" />`
<br>**Detail:** Exact time is optional; [read more here](https://en.wikipedia.org/wiki/ISO_8601).
<br>**Used in:** Page freshness scoring.<br>
<br>
`<meta name="robots" content="..., ..." />`
<br>**Detail:** Use the [meta robots tag]({{ site.baseurl }}/indexing/how-search-engines-index-content-better-discoverability.html#robots) to block the search engine from indexing a particular page.
<br>**Used in:** Used during indexing, does not affect relevance ranking.<br>
<br>
`<main>`
<br>**Detail:** Allows the search engine to target the actual content of the page and avoid headers, sidebars and other page content not useful to search. [Read more about the <main> element here]({{ site.baseurl }}/indexing/how-search-engines-index-content-better-discoverability.html#main-element)
<br>**Used in:** Query matching, term frequency scoring<br>
<br>
`<lastmod>`
<br>**Detail:** This field is included in XML sitemaps to signal to search engines when a page was last modified. Search.gov collects this metadata in case there is no `article:modified_time` data included in the page itself.
<br>**Used in:** Indexing processing, page freshness scoring.<br>
<br>
<br>
