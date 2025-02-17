---
layout: page
title: XML Sitemaps
crumbname: Sitemaps
category: admin-center
redirect_from: 
  - /blog/sitemaps.html
  - /manual/sitemaps.html
tags: sitemaps indexing
date: January 17, 2020
last_modified_at: January 17, 2020
sidenav: indexing
---
An [XML sitemap](https://en.wikipedia.org/wiki/Sitemaps)  is an XML formatted file containing a list of URLs on a website. An XML sitemap provides information that allows a search engine to index your website more intelligently, and to keep its search index up to date. 

Sitemaps tell search engines what URLs are on a website, and, if URLs are added as they are published, they tell the engines what new content needs to be picked up. They may also provide additional metadata about each URL, such as the last modified date, which signals to the engine to update the index record for that page.  

Search.gov uses sitemaps to tell us what URLs should be in our index and when a URL has been updated. Sitemaps are used in a similar way by [Google](https://support.google.com/webmasters/answer/156184) , Bing, and and other search engines. *Having an xml sitemap will improve your Google SEO (search engine optimization).*

Example: [https://search.gov/sitemap.xml]({{ site.baseurl }}/sitemap.xml)

## What content should be on XML sitemap?

Some sitemaps are comprehensive, but for very large sites you may need to publish several sitemaps. Each sitemap should be no more than 50MB or 50,000 URLs, whichever comes first. You do not need to add URLs of content you want to remain unsearchable.

**Note** that an HTML formatted file listing the pages of a site is more akin to an index page, and is not the same as an XML sitemap. HTML files are human friendly, but not machine friendly, and Search engines need an xml formatted file in order to leverage the information for indexing work.

## More than one web platform? Use multiple sitemaps.

It's common for agencies to use more than one platform to publish their websites. For instance, a CMS was launched, but some content is still on the legacy site's platform. In this case, use available plugins for the CMS's in your environment to auto-generate sitemaps for that content. Manually generate a sitemap for any static content. You can publish a [sitemap index file](https://www.sitemaps.org/protocol.html#index)  that lists the locations of all your specific sitemaps, or you can list all your sitemaps on your robots.txt file.

## How do search engines find my sitemap(s)?

Sitemaps (or the [sitemap index](https://www.sitemaps.org/protocol.html#index) ) should be listed in your site’s robots.txt file, i.e.:  
`Sitemap: https://www.example.gov/sitemap_1.xml`  
`Sitemap: https://www.example.gov/sitemap_2.xml`  

List the appropriate sitemap(s) for the domain or subdomain. `www.example.gov/robots.txt` would list sitemaps for content in the `www` subdomain, while `forms.example.gov/robots.txt` would list sitemaps for the `forms` subdomain.

Read more about [robots.txt files]({{ site.baseurl }}/indexing/robotstxt.html), and take a look at ours: [https://search.gov/robots.txt]({{ site.baseurl }}/robots.txt)

## What should my XML sitemap look like?

Please refer to the official [sitemaps protocol](https://www.sitemaps.org/protocol.html)  for full information on how a sitemap should be structured.

When publishing your sitemap, be sure it begins with an `<xml>` declaration, and that the URLs are enclosed in opening and closing tags. To take a simplified example:

```
<?xml version="1.0" encoding="UTF-8"?>
<urlset>
<url>
<loc>https://example.gov/blog/file1.html</loc>
<lastmod>2018-03-19T00:00:00+00:00</lastmod>
</url>
<url>
<loc>https://example.gov/policy/new-policy.html</loc>
<lastmod>2018-03-27T00:00:00+00:00</lastmod>
</url>
</urlset>
```
If you use multiple sitemaps, then you'll need to use a [sitemap index](https://www.sitemaps.org/protocol.html#index) , along these lines:

```
<?xml version="1.0" encoding="UTF-8"?>
<sitemapindex>
<sitemap>https://example.gov/sitemap.xml?page=1</sitemap>
<sitemap>https://example.gov/sitemap.xml?page=2</sitemap>
</sitemapindex>
```
Importantly, be sure that any [special characters in your URLs are escaped](https://www.sitemaps.org/protocol.html#escaping)  so the search engines will know how to read them.

## What metadata does Search.gov require for each XML sitemap URL?

The sitemap protocol defines [required and optional XML tags](https://www.sitemaps.org/protocol.html#xmlTagDefinitions)  for each URL. We recommend including the `<lastmod>` value (the date of last modification of the file) whenever possible, to indicate when a file has been updated and needs to be re-indexed. 

We do not have plans to support the `<priority>` tag, which is [no longer used](https://www.seroundtable.com/google-priority-change-frequency-xml-sitemap-20273.html)  by search engines like Google. We may support the `<changefreq>` tag in the future, but the `<lastmod>` tag is more accurate and supported by more search engines.

## How can I create an XML sitemap?

Most content management systems provide tools to generate a sitemap and keep it updated. Below are some tools that we recommend:

### Drupal
[XML Sitemap Module](https://www.drupal.org/project/xmlsitemap) 

### Wordpress
[Yoast SEO Plugin](https://wordpress.org/plugins/wordpress-seo/) 

[Google Sitemap Plugin](https://wordpress.org/plugins/google-sitemap-generator/) 

### Wagtail
[Sitemap Generator](http://docs.wagtail.io/en/latest/reference/contrib/sitemaps.html) 

### Github Pages (Jekyll)
[Jekyll Sitemap gem](https://help.github.com/articles/sitemaps-for-github-pages/) 

### Online generators
(Note: free online generators often have a limit to the number of URLs they will include, and do not always generate the most accurate sitemaps. Use them only as a last resort.)

[Free Sitemap Generator](https://freesitemapgenerator.com) 

[Web Sitemap](http://www.web-site-map.com/) 

## Sitemap checklist
<i class="icon-check" ></i> 1. One or more sitemaps have been created

<i class="icon-check"></i> 2. The URLs in the sitemap have been reviewed (clean URLs, only includes URLs that should be searchable)

<i class="icon-check"></i> 3. Each sitemap’s XML format has been [validated](https://www.websiteplanet.com/webtools/sitemap-validator/) 

<i class="icon-check"></i> 4. Each sitemap (or a sitemap index) is listed in the site’s robots.txt file

## Additional Resources:
[Official Documentation from Sitemaps.org](https://www.sitemaps.org/) 

[Google’s guide to building a sitemap](https://support.google.com/webmasters/answer/183668?hl=en&ref_topic=4581190) 

[Sitemap validator](https://www.websiteplanet.com/webtools/sitemap-validator/) 

## More questions?
If you have questions that aren't answered here, [email us](mailto:search@support.digitalgov.gov). We'll also keep updating this page over time.
