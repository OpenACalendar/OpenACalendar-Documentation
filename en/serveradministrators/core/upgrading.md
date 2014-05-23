# Upgrading

## Upgrade procedure

Place the new files over the old ones. (If you have had to change any 
"localConfig.php" files to accomodate your webserver, be careful to preserve 
the changes.

Run the PHP script "php core/cli/upgradeDatabase.php".

Run the PHP script "php core/cli/loadStaticData.php".

On servers not in Debug mode, delete the existing cached templates. These are 
found in "cache/templates.cli" and "cache/templates.web". (It doesn't hurt to 
do this on debug servers so if in doubt, just do it.)

## Assets Version and Browser Caching

There are Apache config files includud in the software that turn on browser caching 
for assets, such as images, CSS and JS. This should help speed up subsequent page loads for users. 

However when you update, you must make sure users get the latest version of all assets. Do this using the config variable.

    $CONFIG->assetsVersion = 1

This is appended to the end of all requests. Set this to 1 on a new install and increase the value by 1 
every time you upgrade.

## Minimising downtime when upgrading - Database upgrades

Following the upgrade procedure above means that there is a small period of time during which
the code has been upgraded and the database hasn't. Users may see errors during that time.

This can be avoided. Database changes are designed to be additions that can be upgraded before the code is upgraded.

Check out the new code into a seperate folder. Give this folder the same config.php and extensions as your normal web app.

Then run the PHP scripts "php core/cli/upgradeDatabase.php" and "php core/cli/loadStaticData.php" 
from this seperate folder.

Now update the code in your normal web app. The new DB structure will be in place already; thus minimising downtime.


