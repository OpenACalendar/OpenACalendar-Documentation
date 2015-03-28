# Cron jobs

There is one script to run regularly. This script will take charge of running tasks when relevant.

Run core/cli/runTasksAutomatically.php every 15 minutes or more.

The folder "cache/templates.cli" must be writable be the user Cron jobs run as.

Make sure more than one of the same script is not running at 
the same time as then you may get race conditions. Sometimes this will not matter, sometimes it will.
If you have a large site you will want to increase the intervals to ensure this.

