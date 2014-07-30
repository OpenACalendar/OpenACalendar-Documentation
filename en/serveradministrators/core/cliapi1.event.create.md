# CLI API V1 Create Event

## Since

Available since V1.2.2

Earlier versions had a bug that created bad data and should not be used.

## Script

Call core/cliapi1/createEvent.php

## Parameters - JSON

Pipe in JSON as Standard input.

## Parameters - JSON - Event Object

Pass as "event" variable.

Include:

  *  summary
  *  description
  *  timezone - One of http://www.php.net//manual/en/timezones.php Note the start and end time you specify should be in this timezone, not UTC.
  *  url
  *  start - A datetime object
  *  end - A datetime object
  
The date time object used for start and end should have one of the following:

  *  str - A string representation. This should be very clear; we recommend "YYYY-MM-DD HH:MM:SS" eg "2014-07-01 10:00:00".

## Parameters - JSON - Country Object

Pass as "country" variable.

Pass one of:

  *  code - 2 character country code; eg "GB" or "DE"
  
## Parameters - JSON - Site Object

Pass as "site" variable.

Pass one of:

  *  id - look up in Sysadmin interface.
  *  slug - eg http://demo.hasacalendar.co.uk/ has slug "demo"

## Parameters - JSON - User Object

Pass as "user" variable.

Pass one of:

  *  username
  *  email

## Parameters - JSON - Group Object

Pass as "group" variable.

Pass one of:

  *  id - look up in Sysadmin interface.
  *  slug - eg http://demo.hasacalendar.co.uk/group/2-edinburgh-cat-walkers-group has slug "2"

## Parameters - JSON - Example

    {
        "event":{
            "summary":"Test",
            "start":{
                "str":"2014-08-01 12:00:00"
            },
            "end":{
                "str":"2014-08-01 12:00:00"
            },
            "country":{
                "code":"DE"
            },
            "timezone":"Europe/Berlin"
        },
        "site":{
            "slug":"test1"
        },
        "group":{
            "slug":"1"
        },
        "user":{	
            "email":"james@example.co.uk"
        }
    }


