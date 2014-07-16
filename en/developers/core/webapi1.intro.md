# Web API 1 - Introduction

## Introduction

Web API1 is a read only API.

Almost all end points are fully public. Some End points relate to private user information for that user, and a key is part of the URL.

Apart from that, no key, app or authentication is needed to access this API.

## Multi Site or Single Site Mode

In Multi Site mode, it is important to note whether you access these on the index domain or an actual calendar.

In Single Site mode, this does not matter.

## Common Parameters

For end points that return time in a local timezone, the GET parameter "mytimezone" can be passed. This should be:
  *  One of the timezones that is configured for this calendar - it is from a country that is selected.
  *  In this format http://php.net/manual/en/timezones.php eg "Europe/London"
