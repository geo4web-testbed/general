# First open testbed session

On december 8, 2015, the kickoff of Geonovum's Spatial data on the web testbed took place. 

## Present: 

Linda van den Brink, Marcel Reuvers, Arnoud de Boer (Geonovum), Matthew Pegels, Teun van Sprundel (Spotzi), Dimitri van Hees, Joost Farla (Apiwise), Clemens Portele (interactive instruments), Lieke Verhelst (Linked Data Factory), Paul van Genuchten (GeoCat), John	van Echtelt	(CGI), Anne Jop	de Jong	(Vicrea), Anne	Fintelman	(Defensie), Herman 	Assink (IDgis), Dirk-Willem	van Gulik (Ardytectuur), en Herzo	van der Wal (RWS)

## Agenda: 
- 13:00 Introduction & who’s who
- 13:15 Introduction to the testbed – Linda
- 13:30 Research topic 2 – Spotzi
- 14:30 Break
- 15:00 Research topic 3 – Apiwise
- 16:00 Research topic 4 – Interactive instruments / Geocat / Linked Data Factory
- 17:00 End

## Introduction

Linda gave [an overview][1] of the why, what, when and how of the testbed. 

## Research topic 2 - Spotzi

Teun and Matthew presented their approach for research topic 2. Notes: 

- [plan of approach][2]
- [slides][3]
- Discussion point: Citizens should be able to change / comment on govt data. Why? They have valuable input about their own environment. However, a lot of the Dutch govt datasets are authoritative and not very changeable (i.e. only the govt data owner are allowed to change the data, not citizens). There are different levels of feedback, official channels on the one end vs tweets on the other end of the spectrum; the feedback loop becomes less strong. Spotzi wants to address all levels.
-	Another challenge of topic 2 should be: how should you publish your data, update/maintain the data, how to support the workflows at data owners better than today. 
- Question: Will it be part of topic 2 that the platform also helps users understand the semantics of the data? Otherwise there will be a lot of useless user feedback. Answer: don’t share useless data with the citizen.
- Is the focus on the end user or citizens in general? Focus more on the end user, e.g. a municipal employee.

## Research topic 3 - Apiwise
Dimitri and Joost presented their approach for research topic 3. Notes: 

- [plan of approach][4]
- [slides][5]
- The goal is to make spatial data crawlable, AND usable for machines as well as web developers. The assumption is that data which is published in a machine-friendly way, is also crawlable and usable for web developers.  
- Example use case: Am i allowed to open a bar here?
- Will test different publication methods, formats and APIs. 
- Will also publish APIs to portals like [swaggerhub][6].
- Challenge: Technical limitations, like performance - won’t address or at least not in focus. HTML representation could be really slow, depending on where it's hosted. If so this might affect if/how its indexed by search engines. 
- Challenge: Extending schema.org – this action is limited to suggestions to maintainer. Via Dan Brickley (Google). Dimitri/Joost signed up for schema.org community group and will collaborate with topic 4 on this.
- Challenge: Search engine indexation frequency. No control over this.
- They will document tooling and best practices around SEO for spatial data.
- They want to test the	Dutch URI strategy and a RESTful URI strategy and measure the results
- They will implement Content negotiation for 5 formats.
- Their approach includes engaging a community for topic 3. To engage web developers, they will publish a [ProgrammableWeb][7] blog series, about testbed progress in general; do a worldwide survey among web developers about spatial data on the web related things; and discuss the testbed during meetups. They will continue to facilitate this community after March 2016. 
- They will work in sprints; the first two weeks they will concentrate on getting the first content type, HTML, up and running and crawlable. 
- Insight: Google also crawls dbPedia, which means it knows something about the dbPedia vocabulary.  
- Seeking collaboration with topic 2 to see if it is possible to make links between their data. 

## Research topic 4 - interactive instruments consortium
Clemens, Lieke and Paul present their approach. Notes: 

- [plan of approach][8]
- Slides: [intro][9], [linked data proxy][10]
- There is a lot of overlaop with topic 3, but the focus is more on the realisation of good spatial data on the web on top of the existing workflows and systems (SDI) in the geospatial domain. If the ideas of spatial data on the web are succesful and turn out to offer a lot of added value, data owners will probably go back to the source data and start publishing it in different ways; but doing it on top of the existing SDI is a much smaller step and therefore useful.  
- They are working within the framework of current geospatial standards and realising within GeoNetwork a Linked data proxy on top of WFS. 
- One aspect where topic 4 does not overlap with 2 or 3 is the link with open data portals. ISO19115/119 metadata will be transformed to DCAT to achieve this.
- Challenge: there could be friction between what Linked Data specialists find desirable, what works for search engines and what works for web programmers. According to early findings, search engines only accept simpel json-ld / schema.org structures, while programmable web needs more advanced structuring. They seek collaboration with topic 3 on this. 
- The work is divided within the consortium. interactive instruments will realise the linked data proxy doen, this will be an open source project. The proxy will not cache data and will work without knowledge of the data within the WFS service. It will also perform coordinate transformation. The data in the service will be published in follow-your-nose fashion, i.e. browsable and paginated.
- Challenge: Geometry / spatial part of schema.org is underspecified. Also, schema.org resources are not dereferenceable. This makes it less useful to link your data to the linked data cloud. 
- Question they will tackle within the next two weeks: which extra base register to use in their testbed experimentation. 
- Within the consortium Linked Data Factory works on semantic mappings. Links between data have to be added dynamically, because the data within the WFS service cannot be changed. Links will also be created to external web resources like dbPedia. The mapping between the data in a specific WFS and other resources must be done manually when configuring the linked data proxy. Automatic mapping was unsuccesful. 
- Besides schema.org topic 4 may also compare other geo-vocabularies. 
- Within the consortium GeoCat works on	metadata mappings and implementation in GeoNetwork. There are two ISO19115/119, both from the linked data community. There is an issue related to serving this either with content negotiation, using RDF/XML for DCAT and json-ld content type for schema.org. They will describe this issue but probably not solve it as this is a general data on the web problem.  
- A Restful API on top of CSW (catalog services) will be realised, serving webdeveloper friendly formats. [nationaalgeoregister.nl (NGR)][11] will be harvested and registered with Google as a sitemap for crawling. If succesful, all datasets which are registered in the NGR catalog will be findable via Google. A first test has already been published. XSLT is used for mapping of metadata formats to HTML with microdata.
- Topic 4 team is also working with agile sprints. 
- Issue: publishing too many datasets, especially the same data multiple times with different URLs but the same content. There's a risk that search engines will assume this is spam and will blacklist the URLs. Solution could be to use the same URLs (i.e. the teams of topic 2, 3 and 4 should not republish the same data with different URLs) or use different data. Another solution may be using schema.org:sameAs to indicate resources are the same. 

## Consolidation between research topics
-	All teams have the same way of working, using Github for open communication and Slack for closed communication within and between teams. Discussions are open on Github. 
- Action for all: for cross-topic issues, ask members from other teams to participate in your discussions!
-	Topic 3 has a big overlap with topic 4. Topic 3 will concentrate on finding out what makes data most crawlable and usable to machines and humans, while topic 4 will reuse topic 3's findings and concentrate more on how to publish data according to those findings, using the current SDI.
-	Topic 3 and topic 2 will collaborate to see if links / integrations between data published according to their ideas, using APIs or a platform, are possible. 
-	Topic 3 will collaborate with topic 4 on the challenges around schema.org. Geonovum may also participate in this as it is a standards issue.
-	The issue around multiple publications of the same data and spam, needs to be addressed. Teams will investigate the wisdom of using the same URI strategy. Or find some other way to solve this like using different datasets, different parts of the same datasets, etc. 
- Action Marcel: create a Github issue to discuss the idea of using more / different data within the testbed. List some ideas and others will add theirs. It would be good if the data that gets used in the different topics, is complementary so that all data used in the testbed can form some logical whole and be used to demonstrate sensible use cases. Arnoud de Boer will also partipate in the thinking about this, since he is working on formulating research topic 5, a working prototype based on the testbed results. Requirement: the data has to be already accessible. Apiwise already has the idea of using CBS wijken/buurten (regions) data.  
-	Maybe all topics should use the same use case. We lack use cases that demonstrate the usefulness of linking spatial data. Arnoud will search for suitable use cases; Spotzi is trying to get Bergen op Zoom to participate in the testbed. 

[1]: <<link to presentation introduction>>
[2]: https://github.com/geo4web-testbed/topic2/blob/master/proposal_topic_2
[3]: slides Spotzi (missing)
[4]: https://github.com/geo4web-testbed/topic3/wiki/Crawlable-geospatial-data-using-the-ecosystem-of-the-Web-and-Linked-Data
[5]: https://github.com/geo4web-testbed/topic3/blob/develop/presentations/kickoff/kickoff.md
[6]: https://swaggerhub.com
[7]: http://www.programmableweb.com
[8]: https://github.com/geo4web-testbed/topic4-general/blob/master/Proposal_topic_4_ii_GeoCat_LDF.pdf
[9]: https://github.com/geo4web-testbed/topic4-general/blob/master/meetings/2015-12-08/Topic4-intro-20151208.pdf
[10]: https://github.com/geo4web-testbed/topic4-general/blob/master/meetings/2015-12-08/Topic4-ldproxy-20151208.pdf
[11]: http://nationaalgeoregister.nl