---
layout: default
section: data_events
title: "Geofence record edits."
description: "Accept record changes only if in the vincinety of the original record."
category: section
tags:
  - location
  - permission
---

To make sure that inspectors are in proximity of the record when making changes, this example creates a bounding box around the record and rejects changes when the current device location falls outside.
``` js
function validateLocation() 
  {
  // get location of record
  lat = LATITUDE();
  lng = LONGITUDE();

  // get current location of device
  var location = CURRENTLOCATION();
  var latitude = location.latitude;
  var longitude = location.longitude;

    // check that the device returns a lon/lat
    if (!location) 
    {
      ALERT('No Location Available');
      return;
    }
  // define bounding box 
  var buffer = 0.000300
  var minLatitude = lat - buffer;
  var maxLatitude = lat + buffer;
  var minLongitude = lng - buffer;
  var maxLongitude = lng + buffer;

  //compare device location against bounding box
  if (!(latitude <= maxLatitude && latitude >= minLatitude && longitude <= maxLongitude && longitude >= minLongitude)) {
    INVALID("It looks like you are not close enough to the record to make changes.");
    SETSTATUSREADONLY(true);
  }
}

ON('validate-record', validateLocation);
```
