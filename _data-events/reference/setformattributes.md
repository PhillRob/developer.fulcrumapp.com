---
layout: default
section: data_events
title: "SETFORMATTRIBUTES"
description: "Configure specific device functionality and behaviors at the form level"
category: section
permalink: /data-events/reference/setformattributes/
---

### Description

SETFORMATTRIBUTES allows you to configure specific device functionality and behaviors at the form level. These configuration options help you control what features the user has available, improving the workflow and data quality for that particular form. You can currently control the following:

* Disable adding photos from the camera roll
* Force record to be sync’d upon save
* Control the minimum accuracy required for the GPS location
* Disable the ability to manually move the record location
* Disable the “Save as Draft” feature
* Control photo and video quality settings

### Parameters

`config` Object (__required__) - A configuration object with the following optional properties:

{:.table.table-striped.event-table}
| Property | Type | Description | Default |
|----------|------|-------------|---------|
| `auto_sync_enabled` | boolean | auto-sync this record after saving | user-preference |
| `auto_location_enabled` | boolean | auto-populate the record location | true |
| `auto_location_minimum_accuracy` | integer | minimum accuracy in meters for the auto-populated location | 1500 |
| `manual_location_enabled` | boolean | allow manually changing the record location | false |
| `media_gallery_enabled` | boolean | allow media from the gallery or camera roll | true |
| `photo_quality` | integer | maximum dimension of photos in pixels, or 'native' | user-preference |
| `video_quality` | string | video resolution, one of: 480p, 720p, 1080p, 2160p | user-preference |
| `drafts_enabled` | boolean | allow saving record as a draft | true |

### Examples

```js
ON('load-record', function() {
  var config = {
    auto_sync_enabled: true,
    auto_location_enabled: true,
    auto_location_minimum_accuracy: 10,
    manual_location_enabled: false,
    media_gallery_enabled: false,
    media_capture_enabled: true,
    photo_quality: '2048',
    video_quality: '720p',
    drafts_enabled: false
  };

  SETFORMATTRIBUTES(config);
});
```