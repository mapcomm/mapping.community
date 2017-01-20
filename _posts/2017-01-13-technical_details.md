---
layout: post
title: Technical Background
description: Technical Background for 'Mapping Community'
image: null
author: Jeremy
---

## Technical Background for 'Mapping Community'

This project is all about "open" data. We leverage a range of industry leading open-standards and open-source tools and all of our data is available under open licenses. Further, as much as possible, we aim to deposit our POI data for community groups in the massively popular crowd-sourced alternative to google maps, bing and map quest:  OpenStreetMaps.

### Infrastructure

Our primary server runs [cartoDB](https://github.com/CartoDB/cartodb), an innovative new platform spinning out location-based intelligence and geospatial data visualisations. Carto is a powerful tool, and we're grateful to that development team for making their product open-source. Caro also provides a hosted service for anyone who might be interested in running their own instance. Our own instance of CartoDB sits on a virtual server hosted by the University of Birmingham.

Practitioner groups can use this server to conveniently update their data sets, and the carto server generates a range of map templates which you can use for your group and embed in your own website. However, most of the magic happens in your web browser using javascript tools such as leaflet and openlayers. 

### What's This About OpenStreetMaps?

In seeking to make our data visible and sustainable over the long term, it was hard to imagine a better fit than the [OpenStreetMap project](http://www.openstreetmap.org/about). OSM aims to be a community-generated map of the whole earth and through the dedicated work of amateur mappers, projects like [Missing Maps](http://www.missingmaps.org/), and innovative support of commercial providers who use OSM as a base maps for application development like [MapBox](https://www.mapbox.com) OSM is quickly becoming the de facto standard for online mapping with a high level of data accuracy.[^171161631] There are many reasons to avoid commercial providers like mapquest, google, and bing maps: 

- Their data is unavailable or highly expensive to acquire, even for scholarly researchers - making for a black box that is hard to verify. 
- Because their provision is as a "free" service, these providers reserve the right to terminate the provision at any time.[^171161633] 
- Interfaces such as Google maps' keep each database discrete and self-contained so there is no opportunity to compare databases across groups.
- And perhaps most concerning is the Terms of Service for these products: 
> “you give Google a perpetual, irrevocable, worldwide, royalty-free, and non-exclusive license to reproduce, adapt, modify, translate, publicly perform, publicly display and distribute Your Content through the Service and as search results through Google Services” [according to the google API terms](https://developers.google.com/maps/terms?csw=1)

OSM is not only a viable alternative - in many cases their data is more accurate, and now provides the provision for a huge range of commercial and free mapping and navigation products. With this in mind, for this project, one of our key long-term pathways for making this data visible and sustainable relies on deploying it onto OSM and we plan eventually to set up many of the underlying datasets on our cartoDB platform as augmented replicants of OSM data.

If you'd like to read more about our efforts embed this work within Open Street Maps, check out our [development guide and wish-list](http://mapping.community/2017-01-01-osm-dev-guide.html).

### Project Time-line

We envision this project proceeding in four stages, aptly named "Mapping Community 1.0 - 4.0". The first stage is nearly complete, and the primary work here has involved working closely with community groups to generate new data sets. We aim to have our production CartoDB server up and running with all these data sets in place by April 2017.

For Version 2.0 of Mapping Community, we are working directly with a group of web-developers to generate a series of web-maps that convey demographic detail and layer interesting information on top of our community group points of interest. For this development process, we're collaborating with graphic artists to create a new icon set for our maps, and meeting with practitioners and other researchers into community to plan meta-data structures for mapping-community. We hope to have this work done by June 2017.

In Version 3.0 of Mapping Community, in consultation with the openstreetmap.org, we are developing protocols and [scripts]( http://wiki.openstreetmap.org/wiki/Osmsync) to deploy select sets of our data as [changesets](http://wiki.openstreetmap.org/wiki/Changeset) to openstreetmap. There is an [automated edits code of conduct](http://wiki.openstreetmap.org/wiki/Automated_Edits_code_of_conduct) for OSM, so we're proceeding with care to make sure these additions remain in OSM and are a sustainable input. Additionally, once this is in place, we will offload parts of the database to OSM permanently, so our own PostGIS database hosted through the CartoDB server will represent a replication of the OSM points updated on a regular basis.

For Version 4.0 of Mapping Community, we will draw in scholarly research and media produced about the groups in our database, linking articles and news automatically to groups that are displayed on the map. Alongside a manual literature review (which is already underway) we aim for this portion of development to deploy algorithms that regularly search for new information and add it to our database combining the best of human researchers and robots!

If you can imagine yourself contributing to any aspect of this work described above, we are actively seeking collaborators. Drop us an [email](mailto:j.kidwell@bham.ac.uk)!

## References (from above)

[^171161631]: There is a growing body of research into OSM. For two examples, see Pascal Neis and Alexander Zipf, “[Analyzing the contributor activity of a volunteered geographic information project: The case of OpenStreetMap](http://www.mdpi.com/2220-9964/1/2/146),” ISPRS International Journal of Geo-Information 2 (2012): 146–165 and Mordechai Haklay, “[How good is volunteered geographical information? A comparative study of OpenStreetMap and Ordnance Survey datasets](http://journals.sagepub.com/doi/abs/10.1068/b35097),” Environment and planning B: Planning and design 4 (2010): 682--703.

[^171161633]: Examples abound, but take the now (in)famous example of Google's termination of the highly popular google reader project and recent [termination and re-commercialisation of their "maps engine" product](https://mapsengine.google.com/about/index.html). Similar limits to benevolent behaviour have come from Mapquest, who recently terminated the free offering of their nominatim mapping service.