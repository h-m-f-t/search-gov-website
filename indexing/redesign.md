---
layout: page
title: Checklist for a Successful Website Redesign
crumbname: Redesign Guide
category: admin-center
redirect_from: 
  - /blog/redesign.html
  - /manual/redesign.html
tags: seo site-launch indexing
date: August 30, 2019
last_modified_at: August 30, 2019
sidenav: indexing

---

We often receive questions when an agency conducts a major website upgrade, changes content management systems, or both. We created this checklist to help ensure your redesign is successful. The stages are:

**Ready...**

1\. [Let the Search.gov team know you are launching a new site](#contact-us)

2\. [Develop a reindexing plan](#develop-plan)

**Set…**

3\. [Prepare xml sitemaps and SEO elements](#prep-seo)

4\. [Add a Search Page Alert](#search-page-alert)

5\. [Prepare color scheme updates and new logo to add to Admin Center](#update-brand)

6\. [Prepare updates to your other search features](#update-features)

**Go!**

7\. [Flip the new website live, let us know](#go-live)

8\. [Implement the changes to the search site](#parallel-tracks)

9\. [Results begin to show](#results-show)

**Victory lap**

10\. [Alert Google and Bing that your website has been refreshed](#google-bing)

![Flow chart showing the steps involved in getting the search index ready to go on Search.gov, for a website that’s being relaunched.]({{ site.url }}/assets/img/site/website-relaunch-workflow.png)
[Website relaunch flow chart detailed description](#description)

[Open large version]({{ site.url }}/assets/img/site/website-relaunch-workflow.png)

       

{: #description }

## Ready...

{: #contact-us }

### 1. Let the Search.gov team know you are launching a new site

**Who:**  You, the agency web team

**What:** Send us an [email](mailto:search@support.digitalgov.gov), give us a call, either way, please let us know that you’re working on a redesign of your website. If we know ahead of time, we can help you get your new search experience prepped and in good shape on the day of the relaunch. When you reach out to us, include the planned launch date.

It’s important to plan ahead, because if there are any changes to your site structure, your search results will break, which will lead to frustration for the public as they try to use your new site. This is true for our service, and out on Google and Bing. To avoid an avalanche of `404 not found` errors from your search results, wherever possible, use 301 redirects to send visitors from the old pages to the appropriate new pages. For more on 301 redirects, read tips from [Bing](http://blogs.bing.com/webmaster/2011/10/06/managing-redirects-301s-302s-and-canonicals/) and [Google](https://support.google.com/webmasters/answer/93633). Notify other websites that link to you of the changes.


{: #develop-plan }

### 2. Develop a reindexing plan

**Who:** Search.gov team, in consultation with you, the agency web team

**What:** We will ask you about your search needs for the new site, including what domains you need to include, how you can generate an [xml sitemap]({{ site.baseurl }}/indexing/sitemaps.html), and what SEO supports you’re putting in place in your new templates, like [metadata]({{ site.baseurl }}/indexing/metadata.html) and [other structured elements]({{ site.baseurl }}/indexing/how-search-engines-index-content-better-discoverability.html). Read more about our [indexing process here]({{ site.baseurl }}/get-started/site-launch-guide.html#indexing-workflow).

As part of this discussion, we’ll make some recommendations and likely agree on some action items for your team to consider implementing prior to your launch. If there are any major SEO warning signs in your setup, we’ll let you know.

We’ll also ask you about the timeline for launch, so that we can reserve a time to coordinate [Step 8](#parallel-tracks) with you.

## Set...

{: #prep-seo }

### 3. Prepare xml sitemaps and SEO elements

**Who:** You, the agency web team

**What:** Action items that usually come out of the planning discussions include

* Ensure that each domain and subdomain you want to be searchable launches with an [xml sitemap]({{ site.baseurl }}/indexing/sitemaps.html).
* Add [metadata]({{ site.baseurl }}/indexing/metadata.html) blocks to the `<head>` of your page templates, and Semantic Markup to the `<body>`.
  * Sometimes these pieces are in place, but need to be modified or moved.
* Talk with other web teams to ask them to do the above items on their sites, so you can leverage them when your site searches their site’s content.

{: #search-page-alert }

### 4. Add a Search Page Alert in the Admin Center

**Who:** You, the agency web team

**What:** Use our [Search Page Alert]({{ site.baseurl }}/admin-center/display/system-alert.html) feature to display a “pardon our dust” type message on your results page. For example:
* `We are launching a new example.gov. If your search does not return the content you expected, please check back soon for updated results.`
* Set the status of the alert to `Inactive` and wait for the relaunch.

{: #update-brand }

### 5. Prepare color scheme updates and new logo to add to Admin Center

**Who:** You, the agency web team

**What:** Gather your [new logo and color palette]({{ site.baseurl }}/admin-center/display/brand.html), if needed. Many sites find it helpful to mock up their redesigned results page in a non-production search site &mdash; you can either [clone]({{ site.baseurl }}/admin-center/dashboard/clone-site.html) your existing site or just use the [Add Site]({{ site.baseurl }}/admin-center/dashboard/add-site.html) button to create a totally new one.

**Don’t implement** these changes on your production site ahead of the actual relaunch (that comes in [Step 8](#parallel-tracks), below).

{: #update-features }

### 6. Prepare updates to your other search features

**Who:** You, the agency web team

**What:** When your URL structure changes, this will affect several of our search features. You’ll want to get your updates ready to go, but **don’t implement** them ahead of the relaunch, or people will end up in the wrong places:

* [Domains]({{ site.baseurl }}/admin-center/content/domains.html): make sure your Domains list includes the domains and subdomains that you want included as the default content to search.
* [Collections]({{ site.baseurl }}/admin-center/content/collections.html): make sure your Collections are searching for the right content in the new location.  
* [Best Bets]({{ site.baseurl }}/admin-center/content/best-bets.html): make sure your Best Bet URLs are correct for the content’s new location.
* [Routed Queries]({{ site.baseurl }}/admin-center/content/routed-queries.html): update the target of your Routed Queries, so searchers will end up on the correct page.
* [RSS]({{ site.baseurl }}/admin-center/content/rss.html) feeds should be removed, and re-added from their new locations.

## Go!

{: #go-live }

### 7. Flip the new website live, and let us know

**Who:** You, the agency web team

**What:** When your new website is publicly available, reach out to us by email or phone. This will be our signal to begin our part of [Step 8](#parallel-tracks).

{: #parallel-tracks }

### 8. Implement the changes to the search site

At this point, the work splits into two parallel tracks, with your team and ours working on related items at the same time.

**Who:** You, the agency web team

**What:** Add the updates you prepared in Steps 4, 5, and 6 to the Admin Center for your production search site:

* Set your Search Page Alert to `Active`.
* Update your colors and logo.
* Update your Domains, Collections, Best Bets, Routed Queries, and RSS Feeds as necessary.

**Who:** The Search.gov team

**What:** We complete several backend tasks
* Switch your production search site to use the new index, which will begin empty for your domain(s).
* Tell our indexer to begin working on your domain(s).
  * The time it takes to get your content indexed depends on the number of items you have, and whether you have a crawl delay declared in your `/robots.txt` file. Generally speaking, a few hundred items should be done in an hour or two, a few thousand items should be done in several hours, etc. 

{: #results-show }

### 9. Results begin to show

**What:** Our indexer will first read your sitemap, collect the urls, and then work through them in the order they were collected. We will work at the crawl delay set in your `/robots.txt` file, or 1 request per second, whichever is slower. This delay is the time after we’ve rendered a page, before requesting the next page to render.

## Victory lap

{: #google-bing }

### 10. Alert Google and Bing that your website has been refreshed.

**Who:** You, the agency web team

**What:** Register for the commercial search engines' webmaster tools, if you haven’t already done so.
* [Bing Webmaster Tools](https://www.bing.com/toolbox/webmaster)
* [Google Search Console](https://www.google.com/webmasters/tools/home?hl=en).
* Resources: 
  *[How to move your content to a new location](http://googlewebmastercentral.blogspot.com/2012/04/how-to-move-your-content-to-new.html)*, Google Webmaster Central Blog.
  * In Bing, submit your new [Sitemaps ](https://www.bing.com/webmasters/help/sitemaps-3b5cf6ed) together with the [Content Removal tool](https://www.bing.com/webmasters/help/bing-content-removal-tool-cb6c294d).

If you've undergone a redesign, followed these steps, and your site search results are not what you'd expect, [send us an email](mailto:search@support.digitalgov.gov).
