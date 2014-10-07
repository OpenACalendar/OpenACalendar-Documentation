# Purge Data

## What is purge?

The system administrator can "purge" data from the system.

Deleting data marks it as deleted but still makes it available. Purge attemps to remove the data from the system completely.

Whilst deleting data is undoable, purging data is NOT undoable in any way.

## When to purge?

It is recommended to purge data only as a last resort and not as a routine operation because:
  *  it is NOT undoable in any way.
  *  it may make the history of your site a bit confused. For example, you may be left with edits that appear to have changed nothing.

## How to purge?

Browse the System Administors user interface.

Find the bit of data you want to purge and enter the command "purge password".

The password is set by your server administrator. There is no default value and the feature will not work if a password has not been set.

It is recommended this password is different from any other passwords - an attacker who hacks into your server administrator UI (maybe by sniffing passwords) is bad enought, an attacker who hacks into your server administrator UI and also knows the password to purge data is really bad.

## How to undo a purge?

Go and fetch a backup of your database and files and restore them. There is no other way.
