---
layout: post
title: Technical Background
description: Technical Background for 'Mapping Community'
image: null
author: Jeremy
---

## Technical Background for 'Mapping Community'

This project is all about "open" data. We leverage a range of industry leading open-standards / open-source technical resources and all of our data is available under open licenses. Further, as much as possible, we aim to deposit our POI data for community groups in the massively popular crowd-sourced alternative to google maps, bing and map quest:  OpenStreetMaps.

### Why OpenStreetMaps?

In seeking to make our data visible and sustainable over the long term, it was hard to imagine a better fit than the [OpenStreetMap project](http://www.openstreetmap.org/about). OSM aims to be a community-generated map of the whole earth and through the dedicated work of amateur mappers, projects like [Missing Maps](http://www.missingmaps.org/), and innovative support of commercial providers who use OSM as a base maps for application development like [MapBox](https://www.mapbox.com) OSM is quickly becoming the de facto standard for online mapping with a high level of data accuracy.[^171161631] There are many reasons to avoid commercial providers like mapquest, google, and bing maps: 

- Their data is unavailable or highly expensive to acquire, even for scholarly researchers - making for a black box that is hard to verify. 
- Because their provision is as a "free" service, these providers reserve the right to terminate the provision at any time.[^171161633] 
- Interfaces such as Google maps' keep each database discrete and self-contained so there is no opportunity to compare databases across groups.
- And perhaps most concerning is the Terms of Service for these products: 
> “you give Google a perpetual, irrevocable, worldwide, royalty-free, and non-exclusive license to reproduce, adapt, modify, translate, publicly perform, publicly display and distribute Your Content through the Service and as search results through Google Services” [according to the google API terms](https://developers.google.com/maps/terms?csw=1)

OSM is not only a viable alternative - in many cases their data is more accurate, and now provides the provision for a huge range of commercial and free mapping and navigation products. With this in mind, for this project, one of our key long-term pathways for making this data visible and sustainable relies on deploying it onto OSM and we plan eventually to set up many of the underlying datasets on our cartoDB platform as augmented replicants of OSM data.

If you'd like to read more about our efforts embed this work within Open Street Maps, check out our [development guide and wish-list](http://mapping.community/2017-01-01-osm-dev-guide.html).

### Technical Specifications ###

Our primary server runs [cartoDB](https://github.com/CartoDB/cartodb), an innovative new platform spinning out location-based intelligence and geospatial data visualisations. Carto is a powerful tool, and we're grateful to that development team for making their product open-source. Caro also provides a hosted service for anyone who might be interested in running their own instance. Our own instance of CartoDB sits on a virtual server hosted by the University of Birmingham.

[^171161631]: There is a growing body of research into OSM. For two examples, see Pascal Neis and Alexander Zipf, “[Analyzing the contributor activity of a volunteered geographic information project: The case of OpenStreetMap](http://www.mdpi.com/2220-9964/1/2/146),” ISPRS International Journal of Geo-Information 2 (2012): 146–165 and Mordechai Haklay, “[How good is volunteered geographical information? A comparative study of OpenStreetMap and Ordnance Survey datasets](http://journals.sagepub.com/doi/abs/10.1068/b35097),” Environment and planning B: Planning and design 4 (2010): 682--703.

[^171161633]: Examples abound, but take the now (in)famous example of Google's termination of the highly popular google reader project and recent [termination and re-commercialisation of their "maps engine" product](https://mapsengine.google.com/about/index.html). Similar limits to benevolent behaviour have come from Mapquest, who recently terminated the free offering of their nominatim mapping service.