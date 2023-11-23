# squadmc-maps
Fork of [squadmc-maps](https://github.com/Endebert/squadmc-maps) specialized on maps for Post Scriptum. Used by Post Scriptum version of the [SquadMC](https://github.com/Endebert/squadmc) running at https://psmc.michalletavka.cz/

# Usage

SquadMC works with external maps hosted on maps.squadmc.ende.pro. However, if you wish to host and serve them locally, follow these steps:

 0. `npm install -g yarn`
 1. `yarn install`
 2. `yarn run mapdata`
 3. `yarn run serve`
 4. adapt the baseUrl variable in the squadmc repository (`squadmc/src/App.vue`), to whatever `http-server` tells you
 
# Adding new maps

Adding maps for Post Scriptum is slightly different than for Squad. You need to add following entry into `public/ps/mapdata.json`.

```json
  {
    "name": "Arnhem",
    "url": "/maps/arnhemlane/{z}_{x}_{y}.jpg",
    "bounds": [4000, 4000]
  }
```

The `"bounds"` member is the size of the map. You need to calculate the values based on minimap actor location.
The minimap actor is to be found in Post Scriptum SDK, it is usually called "MapMarker" or "MinimapCorner" or something like that.
There are two actors in opposite corners of the map. You may refer to the original guide for [grabbing the locations](https://github.com/Endebert/squadmc-maps/wiki/How-to-add-new-maps-to-SquadMC#get-minimap-corners-usually-entities-already-exist).

Then use the following formula to calculate the `"bounds"` value.

```
x = (ABS(MapMarker1.x) + ABS(MapMarker2.x)) / 100
y = (ABS(MapMarker1.y) + ABS(MapMarker2.y)) / 100
```

# Creating fotomaps

TBA