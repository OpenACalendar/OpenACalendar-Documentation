# Web API 2 - Introduction

## Introduction

Web API2 is a writeable API with user authentication by an OAuth like procedure.

## Apps

All access must be done by an app.

Currently only system administrators can create apps.

Permissions app can ask for.

* Write User Actions  - write that user is attending events, write to users curated lists
* Write Calendar - write to events, groups, etc

Set callback methods the app is allowed to use. Callback methods are explained more later.

* URL
* Display
* Javascript

This stops stolen app credentials being used to widely. For example, in an Android app the app token and app secret must be in the app and an attacker could extract them. But if this app is configured for is callback javascript only and not is callback url, the attacker can't use those tokens in a web service.

* allowed callback URLs - text field, list them separated by new lines. The start of the callback URL specified later must match one of these. eg If you set allowed callback URLs to http://myserver.com/callback then http://myserver.com/callback/user/348 will pass but http://www.myserver.com/callback/user/348 will fail

## Permissions Escalation

You can set which permissions to ask for, and users will be able to edit permissions given. User can revoke permissions later.

So apps can start by asking for read access only then ask for write access later (by repeating the same process with a different scope parameter). Or they may ask for write access but get read access only. Or they may start with write access but then be bumped down to read access only later.

Apps therefore must always call /api2/current_user.json to check permissions.

Note each user grants permissions once per app. So if a user installs the same app twice (eg Android phone and Android Tablet), they all use the permissions. So if one app asks for and obtains better permissions, the other app will have that permission to.


## Notes

All tokens are random alphanumeric strings that could be between 1 or 255 chars long - the length is picked at random to increase the number of possibilities. Always allow for 255 chars long tokens in your app.

HTTPS should be used if possible. If the site doesn't have SSL installed then that's a security risk, but if so then the normal web login form and session cookies are over HTTP so whatever.

Passing variables can be GET or POST.

At the moment, all responses are JSON as denoted by .json at the end of URLS. We may add .xml and where applicable, .atom, .rss or .ical/.ics later. We may also provide URLs with nothing at the end, in which case the server will use the Accept header to decide what to send back.

A sys admin or app owner will be able to regenerate all user_token and user_secret for that app. This won't change any permissions users has granted, but will mean that all installs of the app have to re-authenticate.

