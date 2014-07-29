# Web API 1 - Show Event

## End points for ICAL

  *  /api1/event/{slug}/info.ical

Slug should be the number only eg /group/1-the-best should become 1.


## End points for JSON

In Multi Site mode, this end point is accesed on the Site pages:

  *  /api1/event/{slug}/info.json

Slug should be the number only eg /group/1-the-best should become 1.


## End points for JSONP

In Multi Site mode, this end point is accesed on the Site pages:

  *  /api1/event/{slug}/info.jsonp

Slug should be the number only eg /group/1-the-best should become 1.

Pass the GET parameter "callback" to specify what javascript function should be called.

