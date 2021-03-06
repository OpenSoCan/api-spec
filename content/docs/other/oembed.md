---
title: "oEmbed"
---

# oEmbed

oEmbed is an open standard for turning a URL into an embeddable piece of content for your site. To find out more about oEmbed [read the spec](http://www.oembed.com/). The App.net oEmbed endpoint will return HTML snippets that you can include on your site. Right now it works for individual posts, and photos.


## oEmbed Endpoint

Returns an oEmbed response for a given URL.

<%= endpoint "GET", "oembed", "None", '', '' %>

<%= url_params [
  ["url", "A URL for a post or photo on App.net."]
]%>

#### Example

> GET https://alpha-api.app.net/oembed?url=https%3A%2F%2Fposts.app.net%2F1

~~~ js
{
    "provider_url": "https://app.net",
    "version": "1.0",
    "author_url": "https://alpha.app.net/mthurman",
    "title": "join.app.net getting ready for the world w/ @dalton @berg @voidfiles @jhubball @aaronblyth @andrew @vinitlee @mark @mintz @barmstrong @laughingman @mikegreenspan @ben #joinus",
    "url": "https://alpha.app.net/mthurman/post/1",
    "provider_name": "App.net",
    "type": "link",
    "html": "...",
    "author_name": "mthurman"
}
~~~

