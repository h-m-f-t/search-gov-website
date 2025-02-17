---
layout: page
title: Add Your RSS Feeds to Our Index
category: admin-center
tags: "help-manual manage-content rss"
date: November 9, 2017
last_modified_at: November 9, 2017
published: true
sidenav: admin_center
redirect_from:
    - /manual/rss.html
---

Find it in the Admin Center: [Search.gov Home]({{ site.baseurl }}/index.html) > [Admin Center](https://search.usa.gov/sites/) > YourSite > Manage Content > RSS

Would you like searchers to be able to search your news or multimedia content? Would you like them to be able to narrow results by date?

Tell us the locations and names of your RSS feeds. We index all new and updated content on your feeds within minutes.

## Step 1. Tell Us About Your RSS Feeds

We love feeds! Tell us about *all* of your RSS feeds, even if you don't opt to show them in step 2 below. Feeds are the fastest and most reliable way for us to learn about your new and updated content.

Select the option to add a new RSS feed.

### Name

Create a name for the feed. Within this 'bucket' you can list a single RSS feed or many feeds. For example, you can opt to list all of your agency's press releases separately (such as Police News, Fire News, EMS News, etc.) or you can list all three under one general name (such as News).

### Feed Type

Select the type of feed. The default option is RSS (for text content like press releases or blogs). Change it to [media RSS](http://www.rssboard.org/media-rss) for multimedia content like images and videos.

Each item within a RSS feed must include a title, link, description, and publication date.

Each item within a media RSS feed must also include both a [media:content URL](http://www.rssboard.org/media-rss#media-content) to specify a direct URL to the media object and a [media:thumbnail URL](http://www.rssboard.org/media-rss#media-thumbnails) to specify a URL to the object's thumbnail.

Any items missing a required element won't display in your search results.

### Sample RSS Item With All Required Elements

	<item>
	<title>
	Statement from Agriculture Secretary Tom Vilsack Regarding World Organization for Animal Health (OIE) Upgrade of United States&apos; BSE Risk Status
	</title>
	<pubDate>May 29, 2013 00:00:00 CDT</pubDate>
	<link>
	https://www.usda.gov/wps/portal/usda/usdahome?contentid=2013/05/0106.xml&contentidonly=true
	</link>
	<description>
	WASHINGTON, May 29, 2013–Agriculture Secretary Tom Vilsack made the following statement about notification received today from the World Organization for Animal Health (OIE) upgrading the United States&apos; risk classification for bovine spongiform encephalopathy (BSE) to negligible risk:
	</description>
	</item>

### Sample Media RSS Item With All Required Elements

	<item>
	<title type="html">
	<![CDATA[ Great Lakes Beach Health ]]>
	</title>
	<link>
	https://gallery.usgs.gov/photos/05_24_2013_gkb4Erq11X_05_24_2013_0
	</link>
	<guid>
	https://gallery.usgs.gov/photos/05_24_2013_gkb4Erq11X_05_24_2013_0
	</guid>
	<pubDate>Fri, 24 May 2013 00:00:00 EDT</pubDate>
	<media:description type="html">
	<![CDATA[ As schools close for the year and summer weather beckons, many recreationalists head to the Great Lakes' public beaches. However, these coastal areas can become 	contaminated with disease-causing bacteria that threaten public health, disrupt water 	recreation, and pay a toll on the Great Lakes economies that depend on summer tourism. ]]>
	</media:description>
	<media:thumbnail url="https://gallery.usgs.gov/images/05_24_2013/gkb4Erq11X_05_24_2013/thumbs/CoastalEco_KPrzybyla_kelly18.JPG"/>
	<media:content type="" url="https://gallery.usgs.gov/images/05_24_2013/gkb4Erq11X_05_24_2013/large/CoastalEco_KPrzybyla_kelly18.JPG"/>
	</item>

## Step 2. Opt to Show As a Facet, Inline Module, or Both

Allow searchers to see inline results for recent, relevant RSS results *across all of your RSS feeds* by turning on the News module on the [Display Overview]({{ site.baseurl }}/admin-center/display/display-overview.html) page. When a searcher’s query matches the title of an RSS article published within the past four months, the article appears in the News module. Very recent news results (less than five days) appear at the top of the page and less recent news results appear at the bottom. Up to three articles are displayed. You can edit the default module title, News, on the Display Overview page.

Allow searchers to narrow results to a specific feed by turning on the option to show the facet on the [Display Overview]({{ site.baseurl }}/admin-center/display/display-overview.html) page. To ensure searchers don't encounter too many dead ends, we recommend showing only feeds with a significant amount of content as a facet.

## Step 3. Check Your Search Results Page

### Module 

If you opted to show your RSS feed(s) as a module, searchers will see inline news results. It will highlight the three most recent, relevant results across all of your RSS feeds.

![RSS Inline Module Example]({{ site.url }}/assets/img/site/RSS-Inline.png)

### Facet

If you opted to show your RSS feed(s) as a facet, searchers can narrow their results to see only RSS-based content by clicking on the facet.

Within the RSS-based results, searchers can opt to limit results to the last hour, day, week, month, or year, or they can set a custom date range. They also can sort results in descending order by relevance (best match first) or date (most recent first).

### Results Count

We show the number of results returned for searches against your feed(s).

![RSS Facet Example with Results Count]({{ site.url }}/assets/img/site/RSS-Facet.png)

## Step 4. Check the Status of Your Feeds

We use [color coding]({{ site.baseurl }}/admin-center/color-codes.html) to indicate each feed's status. 

![RSS status messages and colors](https://d3qcdigd1fhos0.cloudfront.net/blog/img/rss-status.png)

{: .usa-table .usa-table--compact}
| Color | Status | 
| :------------ | :---------------------------------- |
| Green&nbsp;&nbsp;&nbsp; | Feed indexed, no errors&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; |
| Yellow | Pending Indexing |
| Red | Feed indexed, but error in one or more items |
| &nbsp; | &nbsp; |

Click on the name of any feed with an error to see more detailed information about it. Possible error messages follow.

* 404 Not Found
* Feed looks empty
* Description can't be blank
* Title can't be blank
* Missing link field
* Missing pubDate field
* Link is not a valid URL
* Linked URL does not exist (HTTP 404)

---

***Troubleshooting tip:*** We support RSS 2.0 and Atom feeds. Learn more and validate your feeds at:

* [W3C Feed Validation Service](http://validator.w3.org/feed/) (Atom & RSS)
* RSS 2.0 [specification](http://www.rssboard.org/rss-specification) and [validator](http://www.rssboard.org/rss-validator/)
* [Atom syndication format](http://atomenabled.org/developers/syndication/)

***Troubleshooting tip:*** We index the content on your RSS feeds from the time you input them in the [Admin Center](https://search.usa.gov/sites/). To backfill historical content, temporarily modify your RSS feeds to return more results. Leave this larger feed in place for one hour. You can do this during off-hours and you don't need to coordinate with us.

***Pro Tips*** 

You can set up a search box on your website that limits results to your feed.

* Start with the standard form snippet on the [Code Snippets]({{ site.baseurl }}/admin-center/activate/code.html) page under the Activate Search tab. Change the form action to `action="https://search.usa.gov/search/news` and add the following line to limit the results to your feed.<br />`<input type="hidden" name="channel" value="###">`
* The value is the number for your feed ID, which is visible in the URL when you edit your feed in the Admin Center.
* You can click on the 'Preview' option to see the content we have indexed for each of your RSS feeds.

When you [provide us with your YouTube channel]({{ site.baseurl }}/admin-center/content/youtube.html), we'll automatically index the RSS feed for your YouTube channel.
