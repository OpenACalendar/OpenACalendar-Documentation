# Web API 1 - List Events in JSON and JSONP format

## Parameters

  *  includeMedias - boolean "true" or "false", optional, false by default. Whether to include medias attached to the event.

## JSON End Points

In Multi Site mode, these end points are accesed on the Site pages:

  *  /api1/events.json
  *  /api1/group/{slug}/events.json
  *  /api1/tag/{slug}/events.json
  *  /api1/area/{slug}/events.json
  *  /api1/venue/virtual/events.json
  *  /api1/venue/{slug}/events.json
  *  /api1/curatedlist/{slug}/events.json
  *  /api1/country/{code}/events.json
  *  /api1/person/{username}/events.json

Slug should be the number only eg /group/1-the-best should become 1.

Country code is the 2 character code eg GB.

## JSONP End Points

JSONP end points are the same as the JSON end points, except with a ".jsonp" extension.

Pass the GET parameter "callback" to specify what javascript function should be called.

eg:

  *  /api1/events.jsonp?callback=myFunc

