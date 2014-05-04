# Send Specified Email

## Purpose

This is a simple script that sends a email build with a set of parameters you pass it.
This allows you to send monthly emails to lists. 

Note there is a web interface for Calendar Admins to do this as a seperate function, 
but this allows you to automatically script this.

Available since V1.1.2.

## Parameters

To Call script, call with
 * 1st parameter; INI file
 * 2nd parameter; enviroment eg Test

By using different environments and different headers in the INI file you can
do stuff like sending a test email to yourself before sending the real email
to others.

## INI file

Use Headers:

    [Common]
    [EnvironmentTest]
    [EnvironmentReal]

Use Fields under any header:

    Subject="Events coming up"
    SiteID=1
    FromEmail=james@example.com
    FromName=James
    TimeZone=Europe/London
    IntroTXTFile = intro.txt
    IntroHTMLFile = intro.html
    To=hello@example.com

(IntroTXTFile and IntroHTMLFile must be relative to the INI file, not absolute paths!)


To send events from now to the end of a set calendar month:

    Year=2013
    Month=12

To send events for the next number of days:

    Days=31

Optional filters:

    AreaID=1


## Example INI file

    [Common]
    Subject="Events coming up"
    SiteID=1
    FromEmail=james@example.com
    FromName=James
    TimeZone=Europe/London
    IntroTXTFile = intro.txt
    IntroHTMLFile = intro.html
    Days=31
    
    [EnvironmentTest]
    To=james@example.com

    [EnvironmentReal]
    To=biglist@emaillistserver.com

