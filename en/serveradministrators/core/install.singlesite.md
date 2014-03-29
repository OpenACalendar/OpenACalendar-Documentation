# Install Single Site Mode

## Install Single Site Mode

Get the code and place on a web server.

Set up a Postgres database.

Copy config.dist.php to config.php and and edit it.

Run the PHP script "extension.Core/cli/upgradeDatabase.php".

Run the PHP script "extension.Core/cli/loadStaticData.php".

Run the PHP script "extension.Core/cli/createUser.php USERNAME EMAIL PASSWORD sysadmin" 
to create your first user.

Run the PHP script "extension.Core/cli/createSite.php SLUG EMAIL" where slug is something 
like "site". (If the site will always be used in Single Site mode the slug does not matter.)

The folder "webSingleSite" must be served by the webserver. Enable SSL if possible. 
Note there is an .htaccess file in there that Apache must use.

The folder "cache/templates.web" must be writable be the webserver.

Enable some vital cron jobs. Please see the cron pagefor more details.

## Install Single Site Mode where all files are under web root.

You will notice that the code has a filesystem where the webroot is under other code. 
We realise this may make it hard to install on some hosts. You can change the folders 
around so all code is under the web root.

In "webSingleSite", create the folder "oacapp". For security reasons, set up apache not to serve 
this folder using an .htaccess file or other method. 

Move all folders except "webSingleSite" underneath your new "oacapp" folder.

Edit the file "webSingleSite/localConfig.php", and change the constant APP_ROOT_DIR 
so it is defined thus:

    define('APP_ROOT_DIR', __DIR__.DIRECTORY_SEPARATOR.'oacapp'.DIRECTORY_SEPARATOR);

Note when updating in future, be careful not to overwrite this file.
	
The files under "webSingleSite" can now be deployed onto your webserver, and 
the rest of the set up instructions for Single Site Mode followed.
