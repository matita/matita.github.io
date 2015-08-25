---
layout: post
published: true
title: Ideas for clocks web app
---


Since I often need to know what time it is in different cities in the world for work, I'm thinking about writing a simple web app to show me the different times.

Here are the specs:
* clean and simple
* mobile friendly and accessible offline
* it should take Daylight Saving Time into account
* it should be possible to give a name to the clocks (apart from the city)
* autocomplete to add a new city/clock (with actual cities)

Optional
* set a specific time and know what is equivalent in other cities
* manually sort the clocks

## Useful resources

* [free cities API](http://gd.geobytes.com/AutoCompleteCity?q=miami)
* [city details](http://gd.geobytes.com/GetCityDetails?callback=ciao&fqcn=Miami,%20FL,%20United%20States) (doesn't provide DST details)
* [Google Maps API to get DST details](http://stackoverflow.com/questions/55901/web-service-current-time-zone-for-a-city#answer-14988400)
