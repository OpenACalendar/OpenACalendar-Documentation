# Install Multi Site Mode

## Choose domain names

The folder "webIndex" must be served by the webserver, on a single name (eg "www.example.com"). 

The folder "webSite" must be served by the webserver, on a name that allows any 
subdomain to reach it (eg "*.example.com").

There must be a common domain between them (eg in this case, it's "example.com"). This is because cookies are shared among them.

## Let's go!

Get the code and place on a web server.

(If downloading the code as a release from the website, it is complete. If downloading as source code or from Git, you will need to use composer to install libraries. Run "composer install" in the root directory. https://getcomposer.org/ )

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

The folder "webSite" must be served by the webserver, on a name that allows any 
subdomain to reach it (eg "*.example.com"). Enable SSL if possible. 
Note there is an .htaccess file in there that Apache must use.

Note you may have to be careful about the order of the apache virtual hosts to 
make sure that the  "webSite" folder does not get requests intended for the "webIndex" folder.

(You may notice folders "webSysAdmin" and "webSysAdminNotSecure" - these have been deprecated and can be ignored.)

The folder "cache/templates.web" must be writable be the webserver.

Enable some vital cron jobs. Please see the cron page for more details.




