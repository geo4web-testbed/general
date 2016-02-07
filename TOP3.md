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

The challenges listed by topic 3 apply to topic 4 as well. In addition, we want to highlight the following challenges we are facing in our work using the existing data infrastructure.

### 1. Real-time link discovery

Existing datasets are often not structured in ways that allow to establish entity-level links between datasets in real-time using a query. For example, many entries in the Bekendmakingen dataset reference individual addresses, but the information is typically hidden one way or another in textual descriptions that humans can read, but cannot be parsed reliably by machines.

This is one of the the issues that we cannot resolve, but that will require work in the data capturing and management workflows.

### 2. Use cases

Design decisions, for example about the vocabularies to use, the URI strategy used by a proxy, the links to include, etc., will often depend on the use cases that should be supported. While the new Environmental Act provides some background for the work, the associated use cases are not clear enough (to us) to provide sufficient guidance. As a result, our work is partly driven by exploring what can be done, but the value is hard to measure.

### 3. Content negotiation based on media types insufficient

Content negotiation does not support selecting the schemas / vocabularies used in a representation. For example, we need to provide multiple RDF representations of metadata: DCAT for data portals and schema.org for search engines. These representations can all be encoded using the same media types. The approach that we have to take is to use a unique URIs for each representation.
