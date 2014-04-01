# Extension: Post Codes from Open Code Point


## Installation

This extension is included with the core software and only needs to be set up.

## Setting up

Download the Code-Point Open files. Extract them to a directory. 
http://www.ordnancesurvey.co.uk/business-and-government/products/code-point-open.html

Run this command. The last location should be the folder that contains the CSV files you just extracted.

    php extension/AddressCodeGBOpenCodePoint/cli/loadData.php /home/james/OpenCodePoint/Data/CSV/

This will create a whole bunch of new CSV files in the folder extension/AddressCodeGBOpenCodePoint/data/ - these contain just the information we need.

(Note you can re-run this step any time there is a new version of the Code-Point Open files to download. 
The files generated in extension/AddressCodeGBOpenCodePoint/data/ are portable - you can generate them on a dev machine and just copy them to the server.)

Finally, edit your config.php and add AddressCodeGBOpenCodePoint as an extension.
