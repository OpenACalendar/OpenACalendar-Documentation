# Web API 2 - User Authentication Workflow

## Get Request Token

This is called in the app direct to the API, so the user can't see this.

Call /api2/request_token.json

pass:

 * app_token
 * app_secret

One of:

 * callback_url - URL to send user back to.
 * callback_display - boolean, "true". If set, the Access Token will just be shown on screen. Use for CLI scripts that say "Go to this URL, Get an Access Code, Paste it here!"
 * callback_javascript - boolean, "true". If set, Javascript interfaces will be called. This is used for Android apps that can place a WebView on a page and detect JS calls - your app can pick up and continue as soon as a Access Code is granted.

If you request a method your app is not allowed to use, it will be ignored. If you set more than 1, it will be random what happens and that's your fault.

Optional permissions to ask for. If you try to ask for a permission that your app doesn't have, it will be ignored.

 * scope - comma or space separated list of 
   * permission_write_user_actions
   * permission_write_calendar

Optional

 * user_token & user_secret - You may already have Read access for a user, and be asking for write access. In this case you know which user you want back, and if you get back a different user that gets complicated. So pass these, and this request token will be for this user only.
 * state - pass a alphanumeric string of up to 255 chars in length. This will be sent back later. Use this to mitigate against http://homakov.blogspot.co.uk/2012/07/saferweb-most-common-oauth2.html

Get as JSON:

 * request_token

## Redirect User to get user permission

Redirect User in their own web browser to /api2/login.html

Pass:

 * app_token
 * request_token

Here the user is asked to login then approve the app.

If callback_url is set, users web browser is redirected to this url with the GET param:

 * authorisation_token
 * state

(Because this is a GET request, there is a limit to the size of the request. http://stackoverflow.com/questions/7724270/max-size-of-url-parameters-in-get Otherwise we would pass request_token to)

If callback_display is set, authorisation_token will just be shown to user.

If callback_javascript is set, then

* OpenACalendar.accessGranted(authorisation_token,state) is called
* OpenACalendar.accessDenied() is called

## Exchange Authorisation Token for User Token

This is called in the app direct to the API, so the user can't see this.

Call /api2/user_token.json

Pass:

 * app_token
 * app_secret
 * request_token
 * authorisation_token

Get back

 * user_token
 * user_secret
