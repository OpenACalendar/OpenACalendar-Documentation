# The system administrator web UI


## Accessing in Single Site Mode

Note some calendar functions are accessed by going to "/admin". Here you can 
set other users up to be a calendar admin. This is different from being a 
real systems administrator.

Go to "/sysadmin".

Note in this mode you still have to select which site (ie Calendar) you want to work with, 
even thought there is only one.

## Accessing in Multi Site Mode

Go to the site domain configured for the "webSysAdmin" folder.

## Security

Users have to have the sysadmin flag set to access the sysadmin interface. The first user you 
create during installation will be a sysadmin. This user can make other users a 
sysadmin using the sysadmin interface.

On accesing the interface, for extra security the user has to enter passwords again.
As well as the users normal password, an additional password is required to access 
the Sysadmin UI. It is set in config.php.

