# squadmc-maps
Fork of [squadmc-maps](https://github.com/Endebert/squadmc-maps) specialized on maps for Post Scriptum.

Post Scriptum version of [squadmc](https://github.com/Endebert/squadmc) mortar calculator with these maps is running at https://psmc.michalletavka.cz/

# Usage

SquadMC works with external maps hosted on maps.squadmc.ende.pro. However, if you wish to host and serve them locally, follow these steps:

 0. `npm install -g yarn`
 1. `yarn install`
 2. `yarn run mapdata`
 3. `yarn run serve`
 4. adapt the baseUrl variable in the squadmc repository (`squadmc/src/App.vue`), to whatever `http-server` tells you
 
# Adding new maps
 
To learn how to add new maps to this repository yourself, please check out this wiki page: https://github.com/Endebert/squadmc-maps/wiki/How-to-add-new-maps-to-SquadMC
 
I'm looking forward to your contributions!

# Creating fotomaps

TBA