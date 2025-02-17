---
layout: page
title: Analyzing Your Site's Queries
category: admin-center
tags: help-manual analytics queries
date: February 28, 2018
last_modified_at: February 28, 2018
sidenav: admin_center
redirect_from:
    - /manual/queries.html
---

Find it in the Admin Center: [Search.gov Home]({{ site.baseurl }}/index.html) > [Admin Center](https://search.usa.gov/sites/) > YourSite > Analytics > Queries

The Queries page lists the number of times a search query (that is, a word or string of words) was entered in the search box on your site by a unique searcher.

Data are shown for the present month-to-date by default. You can change the time period by selecting a different month or year and re-generating the report.

You can also toggle between filtered and unfiltered views of the data by clicking on the filter icon (<i class="icon-filter"></i>) in the top navigation bar. The filtered data represent our best effort to show you real searches performed by your site's visitors. The unfiltered data include nearly all searches and clicks. Only known spiders (such as Bingbot and Googlebot) are excluded.

Data are available in the Admin Center from the past 13 months.

## Top Queries

***Top 1,000.*** You'll see a list, in frequency order, of the 1,000 most popular queries for your selected time period. 

***Top 1,000 by query.*** Enter any specific term or phrase into the Query search box. Re-generate the report to see the top 1,000 queries that contain that term or phrase and its stemmed equivalents. 

For example, below are the top 10 queries related to *housing* on USA.gov in August 2013.

1. house of representatives
2. housing
3. speaker of the house
4. white house
5. house minority leader
6. housing assistance
7. house majority leader
8. speaker of the house 2013
9. the white house
10. houses

## Download Details

You can download a detailed CSV (comma separated values) file for any search term. There's one line for each time this query was run. This CSV file gives you access to the raw search logs, including:

* The date and time of the query
* The query (It is embedded in the request URL. Look for the text following ‘query=’.) 
* Where the person was when they ran the search (We use the ISO-2 alpha standard for country codes and ISO 3166-2 codes for country subdivisions.)
* The modules loaded in response to the query (Our [Module Codes]({{ site.baseurl }}/admin-center/analytics/module-codes.html) page provides a key of the codes and names.)
* The kind of device and browser they were using
 
## Clicks From a Query and Queries Leading to a Click

Select "View Clicks" to view the top clicked URLs for each query.

If you clicked on "View Clicks" for the *house of representatives* example above, you'd see that the top URLs clicked for that query are:

1. www.house.gov
2. www.house.gov/representatives
3. www.house.gov/representatives/find

From this list of clicked URLs, you'd be able to select "View Queries" to view the top queries that led to a click for each URL.

If you clicked on the first-listed *www.house.gov* in the example above, you'd see that the top queries leading to a click on that URL are:

1. house of representatives
2. congress
3. congress members
4. congress representatives

You can loop through or drill down into this list for any set of clicks and queries.

## Click-through Rate (CTR)

The click-through rate (CTR) is the the number of clicks from a query divided by the number of queries (multiplied by 100 to be expressed as a percentage).

High or low CTR's may indicate that users are not able to find relevant results. A CTR can be over 100%: if a user enters a query, clicks on a link, hits 'back' in their browser, returns to the search results, and clicks again, the CTR for that query would be 200% (2 clicks divided by 1 query, multiplied by 100 = 200%).

---

***Pro Tip*** 

The [Monthly Report]({{ site.baseurl }}/admin-center/analytics/monthly-reports.html) section gives a bird's-eye view of the number of queries and [clicks]({{ site.baseurl }}/admin-center/analytics/clicks.html) on your site each month. The [Site Overview]({{ site.baseurl }}/admin-center/dashboard/site-overview.html) provides a snapshot of what has been happening on your site in the past day or so.
