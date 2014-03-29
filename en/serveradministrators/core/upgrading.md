# Upgrading

Place the new files over the old ones. (If you have had to change any 
"localConfig.php" files to accomodate your webserver, be careful to preserve 
the changes.

Run the PHP script "php extension.Core/cli/upgradeDatabase.php".

Run the PHP script "php extension.Core/cli/loadStaticData.php".

On servers not in Debug mode, delete the existing cached templates. These are 
	found in "cache/templates.cli" and "cache/templates.web". (It doesn't hurt to 
	do this on debug servers so if in doubt, just do it.)

