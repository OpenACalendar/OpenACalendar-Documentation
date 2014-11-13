# Web API 2 - Edit Venue

_Note the current version of this API is still in progress, and some details may change_

Call:
  *  POST request to /api2/venue/xx/info.json

xx is the slug - eg 4

Authentication [with app and user](/en/developers/core/webapi2.callauthentication.md) is required.


Parameters:
  *  title
  *  description
  *  address
  *  address_code
  *  lat & lng - these must be specified together

