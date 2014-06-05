# Cron jobs

Some PHP scripts need to be configured to run as Cron jobs.

The folder "cache/templates.cli" must be writable be the user Cron jobs run as.

For all scripts, make sure more than one of the same script is not running at 
the same time as then you may get race conditions. Sometimes this will not matter, sometimes it will.
If you have a large site you will want to increase the intervals to ensure this.

## core/cli/runImportURL.php

This imports data from other URLs. If you have this feature turned off, you can ignore this.

Recommended interval: every hour.

Parameters: none.

## core/cli/sendUpcomingEventsForUser.php

This should only be run once per day.

Recommended interval: Once per day only. 

Parameters: pass "yes" as first parameter to make this actually run.

## core/cli/sendUserWatchesGroupNotifyEmails.php



Recommended interval:  every hour.

Parameters: pass "yes" as first parameter to make this actually run.

## core/cli/sendUserWatchesGroupPromptEmails.php



Recommended interval:  once per day.

Parameters: pass "yes" as first parameter to make this actually run.

## core/cli/sendUserWatchesSiteGroupPromptEmails.php



Recommended interval:  once per day.

Parameters: pass "yes" as first parameter to make this actually run.

## core/cli/sendUserWatchesSiteNotifyEmails.php



Recommended interval:  every hour.

Parameters: pass "yes" as first parameter to make this actually run.	

## core/cli/sendUserWatchesSitePromptEmails.php



Recommended interval:  once per day.

Parameters: pass "yes" as first parameter to make this actually run.

## core/cli/updateAreaBoundsCache.php



Recommended interval:  every hour.

Parameters: none.

## core/cli/updateAreaFutureEventsCache.php



Recommended interval:  every hour.

Parameters: none.

## core/cli/updateAreaParentCache.php



Recommended interval:  every hour.

Parameters: none.

## core/cli/updateSiteCache.php



Recommended interval:  every hour.

Parameters: none.

## core/cli/updateHistoryChangedFlags.php

Recommended interval:  every hour.

Parameters: none.
