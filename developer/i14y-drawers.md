---
layout: page
title: Working With i14y Drawers
category: developer
tags: "help-manual manage-content i14y"
date: October 3, 2017
last_modified_at: October 3, 2017
sidenav: support
published: true
redirect_from:
    - /manual/i14y-drawers.html
---

{% include archive.html %}

[Search.gov Home]({{ site.baseurl }}/index.html) > [Admin Center](https://search.usa.gov/sites/) > YourSite > Manage Content > i14y Drawers

An [i14y]({{ site.baseurl }}/developer/i14y.html) Drawer is an index receiving content via the i14y API. We've called them **Drawers** because, like drawers in a filing cabinet, multiple indexes can be included in a single configuration to scope the entirety of a site’s search.

Information on working with our Drupal module is [here]({{ site.baseurl }}/developer/drupal.html).

## Step 1. Make sure your site is connected to i14y

If your site Admin Center has the following page: [Admin Center](https://search.usa.gov/sites/) > YourSite > Manage Content > i14y Drawers, your site is connected to i14y. If you don't see this page in the Admin Center, [email us](mailto:search@support.digitalgov.gov). You can also read about [Getting Started with i14y]({{ site.baseurl }}/developer/i14y.html).

## Step 2. Add one or more Drawers
On [Admin Center](https://search.usa.gov/sites/) > YourSite > Manage Content > i14y Drawers, Click `Add i14y Drawer` in the upper right corner. If you have more than one website that will be sending content, add a separate Drawer for each of these sites.

### Handle

Let us know what the handle for your drawer should be &mdash; the handle must be all lowercase alphanumeric, all one word, and can include underscores but no other special characters (e.g., agency_drawer_handle2).

The Drawer *Description* is optional

## Step 3. Send Content to Fill your Drawer

After you have created your Drawer(s), click `Show` from the i14y Drawers list to find that Drawer’s secret API key. Use this secret key with your drawer handle in your API call or your CMS module to [send your content to the right place]({{ site.baseurl }}/developer/indexing-api.html).

## Step 4. Review your Index

You can view the number of documents indexed for each drawer on the main i14y Drawers list, and when the most recent document was received. Click `Show` to view documents within a particular drawer. We display the most recent 1,000 items that were sent to the drawer. You can also search for keywords in the documents' text, titles, and descriptions (Note: you cannot currently search for URLs).

**Note:** We use the [Domains]({{ site.baseurl }}/admin-center/content/domains.html) section to scope search results &mdash; if the domain(s) of your i14y content are not listed in the Domains section, that content will not appear on your search results page. 

We send success and / or failure codes in response to your API call, so if the number of documents in our index doesn’t match what you sent, check those response codes.

***Note:*** If you experience difficulty sending documents to i14y, it is possible your firewall is not letting you communicate with the i14y server. Check out our [cURL test commands]({{ site.baseurl }}/developer/i14y-testing.html) or view the full [i14y documentation]({{ site.baseurl }}/developer/indexing-api.html).

---
***Caution:*** A pop-up message will appear when you hit `Remove` on a drawer: please review this pop-up message carefully. If you remove a drawer that is only associated with one search configuration, the drawer and its contents will be deleted from our system. If the drawer is attached to multiple search configurations, it will only be removed from the search configuration you are currently on. The pop-up message will indicate what type of drawer you have.

If you accidentally delete a drawer, you will need to set up a new drawer and resend the content &mdash; we are unable to retrieve deleted drawers. If you accidentally remove a shared drawer but it is still associated with other search configurations, we can re-attach it to your site. [Contact us](mailto:search@support.digitalgov.gov) for assistance.

---
***Pro Tip*** 

We can attach each i14y drawer to multiple search configurations: if you have a drawer that you’d like to use for multiple search sites, [email us](mailto:search@support.digitalgov.gov).
