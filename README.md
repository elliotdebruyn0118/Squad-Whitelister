# Squad-Whitelister

This is based built on https://github.com/fantinodavide/Squad_Whitelister/releases
<br>Specifically, version 1.3.16 (the latest as of creating this repo)

<br><br><br>

# Installation
<br>1. Use the basic installation found here for the base stuff: https://github.com/fantinodavide/Squad_Whitelister/releases
<br>2. Edit conf.js to your needs
<br>
<br>3. MOST IMPORTANT PART, EDIT THESE LINES IN `SERVER.JS`:
<br>• Line 2687-2690 (All 'replace' values) - this will be the MySQL database connection for your SquadJS server 1 database
<br>• Line 2803-2806 (All 'replace' values) - this will be the MySQL database connection for your SquadJS server 2 database (if it's the same database as SquadJS server 1, then use the same values)
<br>
<br>WARNING: Make sure that your SquadJS server 2, even if on a seperate database, is using id `2` for the server ID, otherwise the bot won't be able to fetch the current map

<br><br><br>
# Main Changes
<br>• Added support for 2x SquadJS servers
<br>• Added a check for current map (this is why the database connection is needed) - It checks DBLog_Matches and then gets the latest match layerClassname based on highest ID and the correct server ID
<br>(This currently checks for if the map includes `seed` or `seeding`)
<br>• Added a fix for losing seeding progress when above seeding threshold
<br><img src="https://user-images.githubusercontent.com/92147251/237039025-d58b60a4-f120-43e9-9b24-a6edd733f9de.png">
