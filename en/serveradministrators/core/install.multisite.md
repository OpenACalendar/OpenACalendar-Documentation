# Install Multi Site Mode

Get the code and place on a web server.

Set up a Postgres database.

Copy config.dist.php to config.php and edit it.

Run the PHP script "core/cli/upgradeDatabase.php".

Run the PHP script "core/cli/loadStaticData.php".

Run the PHP script "core/cli/createUser.php USERNAME EMAIL PASSWORD sysadmin" 
to create your first user.

Create the demo calendar. Run the PHP script "core/cli/createSite.php SLUG EMAIL" 
where slug was set in your config.

The folder "webIndex" must be served by the webserver, on a single name (eg "www.example.com"). 
Enable SSL if possible. Note there is an .htaccess file in there that Apache must use.

The folder "webSysadmin" must be served by the webserver, on a single name (eg "sysadmin.example.com"). 
Ideally, only serve this over SSL. Note there is an .htaccess file in there that Apache must use.

The folder "webSite" must be served by the webserver, on a name that allows any 
subdomain to reach it (eg "*.example.com"). Enable SSL if possible. 
Note there is an .htaccess file in there that Apache must use.

Note you may have to be careful about the order of the apache virtual hosts to 
make sure that the  "webSite" folder does not get requests intended for the "webIndex" or 
"webSysAdmin" folders.

The folder "cache/templates.web" must be writable be the webserver.

Enable some vital cron jobs. Please see the cron page for more details.




