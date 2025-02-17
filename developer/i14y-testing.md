---
layout: page
title: cURL Commands For i14y Testing
category: developer
tags: i14y api manage-content
date: April 12, 2018
last_modified_at: April 12, 2018
sidenav: support
---

{% include archive.html %}

> **Important Note:** April, 2018. i14y does not visit your content to do full-text scraping of your content. For new implementations, the Search.gov team recommends you index your content with us not using the i14y API, but rather by publishing a comprehensive xml sitemap, which we can use to index your content. [Read more.]({{ site.baseurl }}/blog/six-months-in.html)

If you experience difficulty sending documents to our index via [i14y]({{ site.baseurl }}/developer/i14y.html), it is possible your firewall is not letting you communicate with the i14y server. Adding a test document to your i14y drawer can help you diagnose a firewall issue.
Windows users may need to [install cURL](https://curl.haxx.se/download.html) in order to run this test from the command line.

## Adding the Test Document

From the command line, enter:

```
curl "https://i14y.usa.gov/api/v1/documents" -XPOST -H "Content-Type:application/json" -u your_drawer_handle:your_secret_token -d '{"document_id":"1", "title":"Test Document", "path": "http://www.gov.gov/cms/doc1.html", "created": "2015-05-12T22:35:09Z", "description":"The summary of the document goes here.", "content":"This is placeholder text, and in a real document would be paragraphs long.", "promote": false, "language" : "en", "tags" : "tag1, another tag"}'
```

Note: you need to replace **your_drawer_handle** with your i14y drawer handle, found in the i14y drawers section in the Search Admin Center ([Search.gov Home]({{ site.baseurl }}/index.html) > [Admin Center](https://search.usa.gov/sites/) > YourSite > Manage Content > i14y Drawers). You will also need to replace **your_secret_token** with the drawer’s secret token, which can be found by hitting “Show” in the 14y drawer list. The drawer handle and token should be separated by a colon (:) with no spaces on either side of the colon.

The above command returns JSON structured like this:

```
{
"status":200,
"developer_message":"OK",
"user_message":"Your document was successfully created."
}
```

If you do not see a 200 status, [contact our team](mailto:search@support.digitalgov.gov).

After successfully sending a document, you should see an increase (by 1) in the number of documents in your [i14y drawer]({{ site.baseurl }}/developer/i14y-drawers.html).

## Removing the Test Document

Once you have successfully added the test document to your drawer, you will need to delete it, or it will appear in your site’s search results.

From the command line, enter:

```
curl "https://i14y.usa.gov/api/v1/documents/1" -XDELETE -u your_drawer_handle:your_secret_token
```

The above command returns JSON structured like this:

```
{
"status":200,
"developer_message":"OK",
"user_message":"Your document was successfully deleted."
}
```

---

***Resources:*** Read tips on [Getting Started With i14y]({{ site.baseurl }}/developer/i14y.html), or view the full [i14y technical documentation]({{ site.baseurl }}/developer/indexing-api.html).
