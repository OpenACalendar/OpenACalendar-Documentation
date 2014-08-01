# Config vars

To see what default options are set, see the file core/php/Config.php


## Database

### databaseType


"pgsql" is the only current option.


### databaseName



### databaseHost



### databaseUser



### databasePassword




## Site Mode

### isSingleSiteMode


Boolean.


### singleSiteID


If single site mode, put the ID of the site to use here. If you have created the DB from scratch this should be 1.


### siteSlugReserved


Array. If Multi site mode, users will not be allowed to create sites with these slugs.


### siteSlugDemoSite


If Multi site mode, this site is a "demo" site that users are directed to as a playbox.



## Web Addresses

Index, Site and Sysadmin need to be different in multi site mode. In single site mode, just set each one to be the same.

Each domain should not include the protocol, eg "example.com" not "http://example.com"

Each domain can include a port number, eg "example.com:1234". This is most useful on dev servers.

### webIndexDomain



### webSiteDomain



### webSysAdminDomain



### hasSSL


Boolean


### webIndexDomainSSL



### webSiteDomainSSL



### webSysAdminDomainSSL



### webSiteAlternateDomains


Array. These are other domains that the site will recognise and redirect to.


### webCommonSessionDomain


This is the session for the cookie. In single site mode, just set the same domain. 
In multi site mode, it needs to go across all domains so set a common parent.


## Site State

### isDebug


Boolean, is site in debug mode.


### siteReadOnly


Boolean. Can lock whole site during upgrades, maintenance, etc.


### siteReadOnlyReason


String. Shown to user.


### extensions


Array. List of extensions active.



## Site identity and contact details

### siteTitle



### emailFrom


Email address


### emailFromName


Name that is shown with email address


### contactTwitter


Username only.


### contactEmail


Email address.


### contactEmailHTML


This is the address that is show on the web page. You may wish to do something so spam bots find it harder to scan.


### facebookPage



### googlePlusPage



### ourBlog


	
## Media

Media is uploaded pictures.

### fileStoreLocation


Location of file store. This should be backed up.


### mediaNormalSize


Number. Size in pixels.


### mediaThumbnailSize


Number. Size in pixels.


### mediaQualityJpeg


Number.


### mediaQualityPng


Number.


### mediaBrowserCacheExpiresInseconds


Number.


### cacheSiteLogoInSeconds


Number. For sites in multi site mode, they can specify that a piece of media is their logo. How long to cache it?

	
## Security and Antispam

### allowNewUsersToRegister


Boolean.


### newUsersAreEditors


Boolean.

	
### bcryptRounds


Number.


### newUserRegisterAntiSpam


Boolean.


### contactFormAntiSpam


Boolean.



## Sys admin interface

### sysAdminExtraPassword


Sys admin users have to enter an extra password to access the sys admin interface. 
Set here as a plain text string.


### sysAdminTimeZone


Time Zone used when browsing the Sys Admin interface.


### sysAdminLogInTimeOutSeconds


Number.


## Analytics

### piwikServerHTTP



### piwikServerHTTPS



### piwikSiteID



	
## New Sites

When you create a site, what features are on by default? Most of these can be changed later in calendar admin.

### newSiteHasFeatureMap


Boolean


### newSiteHasFeatureCuratedList


Boolean


### newSiteHasFeatureImporter


Boolean


### newSiteHasFeatureGroup


Boolean


### newSiteHasFeatureVirtualEvents


Boolean


### newSiteHasFeaturePhysicalEvents


Boolean


### newSitePromptEmailsDaysInAdvance


Number


### newSiteHasQuotaCode


This should be a Quota level you have already set up in the sys admin interface. "BASIC" is configured by default.

	
	
## Misc

### cacheFeedsInSeconds



### clockDisplayDefault


"12hr" or "24hr".


### assetsVersion


All assets (CSS, Images, Js, etc) have this appended to the URL. You can tell 
browsers to cache all assets, and increment this when you update assets to make 
sure browsers get the latest ones. See [the upgrading guide](/en/systemadministrators/core/upgrading.md) for more.


### eventsCantBeMoreThanYearsInFuture



### eventsCantBeMoreThanYearsInPast



### calendarEarliestYearAllowed



### userAccountVerificationSecondsBetweenAllowedSends



### tmpFileCacheLocation



### tmpFileCacheCreationPermissions



### logFile



### logFileParseDateTimeRange



### sessionLastsInSeconds



### resetEmailsGapBetweenInSeconds



### userWatchesGroupPromptEmailShowEvents



### userWatchesSitePromptEmailShowEvents



### userWatchesSiteGroupPromptEmailShowEvents



### userWatchesPromptEmailSafeGapDays



### importURLExpireSecondsAfterLastEdit



### importURLSecondsBetweenImports



### importURLAllowEventsSecondsIntoFuture



### upcomingEventsForUserEmailTextListsEvents



### upcomingEventsForUserEmailHTMLListsEvents



### siteSeenCookieStoreForDays



### apiExtraHeader1Html

When HTML is sent from the API, extra content can be added. Use for links to surveys, etc.

### apiExtraHeader1Text

When Text is sent from the API, extra content can be added. Use for links to surveys, etc.


### apiExtraFooter1Html

When HTML is sent from the API, extra content can be added. Use for links to sponsors, etc.

### apiExtraFooter1Text

When Text is sent from the API, extra content can be added. Use for links to sponsors, etc.

### canCreateSitesVerifiedEditorUsers

Since v1.2.2. Can verified users create sites from the web index pages. Boolean.


