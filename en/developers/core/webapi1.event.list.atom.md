# Web API 1 - List Events in ATOM format

There are 2 different set of ATOM end points.

One lists events as they are created. This is useful for keeping an eye on a calendar.

The other lists events a certain number of days before they start. This is useful for getting notifications of upcoming events.


## Endpoints for a feed as events are created

  *  /api1/events.create.atom
  *  /api1/group/{slug}/events.create.atom
  *  /api1/tag/{slug}/events.create.atom
  *  /api1/area/{slug}/events.create.atom
  *  /api1/venue/{slug}/events.create.atom
  *  /api1/venue/virtual/events.create.atom
  *  /api1/curatedlist/{slug}/events.create.atom
  *  /api1/country/{code}/events.create.atom

Slug should be the number only eg /group/1-the-best should become 1.

Country code is the 2 character code eg GB.

## Endpoints for a feed before events

  *  /api1/events.before.atom
  *  /api1/group/{slug}/events.before.atom
  *  /api1/tag/{slug}/events.before.atom
  *  /api1/area/{slug}/events.before.atom
  *  /api1/venue/{slug}/events.before.atom
  *  /api1/venue/virtual/events.before.atom
  *  /api1/curatedlist/{slug}/events.before.atom
  *  /api1/country/{code}/events.before.atom

Slug should be the number only eg /group/1-the-best should become 1.

Country code is the 2 character code eg GB.

Pass the optional parameter "days" to set how many days. Eg:

  *  /api1/events.before.atom?days=5

