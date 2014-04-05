# Documentation - the technical details

## In git!

All documentation is stored in Git. Please 
[make any changes you want and submit a pull request](https://github.com/OpenACalendar/OpenACalendar-Documentation).

The git repository is branched for each major and minor version.

  *  master - the latest documentation
  *  v1.1.x - branch for all v1.1.? releases

## Folders

In the repository, there are a series of folders. Your documentation should be in a series of folders.

First, the language.

Secondly, the audience it is intended for.

Thirdly, is it for the core of the system or an extension. Anything that doesn't explicetly belong in a extension should be in core.

## Documentation Files

All documentation is a markdown file with a ".md" extension. Follow standard markdown rules with these exceptions.

### Links

To link to one file from another, use a relative link with the path in the repository and the name of the file with the markdown extension. Eg

````
If you aren't sure if you want [Single Site or Multi Site mode, read up on them 
first](/en/systemadministrators/core/singlesiteormultisite.md) and choose.
````

When the Markdown is compiled to a webpage this will be rewritten with the proper link.

### Don't use index.md

When we compile the documentation we add a index file.

## index.txt file

In each folder, you can have a index.txt file.

This is used when generating HTML to control the listings of folders - both the order and the actual text that appears.

Each folder or file in the folder should have a single line entry. The order these appear in is the order they will appear in on the website.

Each line should have up to 3 fields.

  *  the name of the markdown file without the extension or folder it is referencing. required.
  *  the label to use when showing the entry. optional.
  *  a short description to show after the label. optional.

An example from /en/index.txt

````
systemadministrators \ System Administrators \ For User with access to the System Administrator Web UI
serveradministrators \ Server Administrators \ For Server Administraters installing and updating the app
contributors \ Contributors \ Writing your own extensions and conbtributing to core or documentation
````

An example from /en/serveradministrators/core/index.txt. note you do note add the ".md" extension.

````
install \ Install Guide 
install.singlesite \ Install Guide for Single Site Mode 
install.multisite \ Install Guide for Multi Site Mode 
cron \ Installing regular cron jobs 
upgrading 
extensions 
````

It is not required to add a entry to the index.txt - any files or folders with no entry will still be listed.