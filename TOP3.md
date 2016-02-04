# Top 3

This document is meant to describe the top 3 challenges for each research topic.

## Research topic #2

...

## Research topic #3

### 1. Crawlability

Goal is to find the most optimal way of publishing spatial data so that search engines can understand and index the data including its spatial properties. Because we don't exactly know how crawling algorithms interpret the data, we must use trial and error to see which combination of URI strategies, vocabularies, datasets, output format, etc. performs best in search engine results. To say something useful about this we need lots of data and index actions, which takes a lot of time.

### 2. Content negotiation

Content negotiation can be used to serve multiple media types for different purposes using the `Accept` header. However, search engines and lots of other clients do not support this way of content negotiation which means we should provide alternative ways like adding parameters or extensions to the URIs. This is conflicting with best practices of content negotiation. Apart from this we should ask ourselves whether we want to return the same same data or want to alter the structure of the data as well. For example: do we publish WKT or GeoJSON in the `application/ld+json` media type?

### 3. Performance & data compactness

Google recommends to serve pages within a response time of [under 200ms](https://developers.google.com/speed/docs/insights/Server). Faster pages are
likely to rank higher in search results. Furthermore, modern web applications need
fast data endpoints with compact response payloads to be able to provide a snappy
user experience and be consumable for low bandwidth devices like smartphones.

## Research topic #4

...
