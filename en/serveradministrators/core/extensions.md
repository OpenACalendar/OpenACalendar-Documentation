#Extensions

Extensions hold templates, setup information, code and assets (JS, CSS, Images). 
An extension can be added to add additional functionality and theme assets.

## Installing an extension

Check the extension documentation for additional instructions, but the basic process 
is simply to add the folder into the "extension" folder in the root of the app. 
Then edit config.php and add the extension.

Note the name of the extension is referenced inside the extension to, so you can 
not rename extensions at will.

Extensions can provide assets (JS, CSS, Images) and you may need to run the 
build scripts to copy the right assets into the web folders after installation.


