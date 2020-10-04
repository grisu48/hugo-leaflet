# Hugo Leaflet

Shortcodes for inserting a OSM (Open Street Maps) Map into your posts by using leaflet.

_You can use as much Maps in a single post as you like! (You only have to load the script once)_

### Quick Start guide

In your hugo post/page, load the scripts once

    # Pick one of the two
    {{< load-leaflet-local >}}   # use local scripts
    {{< load-leaflet >}}         # load scripts via CDN

And then place maps ecc.:

    # Map only
    {{< leaflet-simple mapHeight="[MAPHEIGHT]" mapWidth="[MAPWIDTH]" mapLon="[MAPLON]" mapLat="[MAPLAT]" zoom="[ZOOM]">}}
    # Map with Marker
    {{< leaflet-simple mapHeight="[MAPHEIGHT]" mapWidth="[MAPWIDTH]" mapLon="[MAPLON]" mapLat="[MAPLAT]" markerLon="[MARKERLON]" markerLat="[MARKERLAT]">}}
    # Map with Marker with Popup
    {{< leaflet-simple mapHeight="[MAPHEIGHT]" mapWidth="[MAPWIDTH]" mapLon="[MAPLON]" mapLat="[MAPLAT]" markerLon="[MARKERLON]" markerLat="[MARKERLAT]" markerContent="[MARKERCONTENT]">}}

---

## Installation/Loading necessary scripts

[Download the project as ZIP](https://github.com/L1am0/hugo-leaflet/archive/master.zip) Place the contents of `layouts` and `static` (required for script local only) in your hugo directory.

### Load Scripts from CDN

1) Copy the `layouts` folder over (containing the shortcuts)
2) Call the load shortcut in every post or globally in the theme

    {{< load-leaflet >}}

### Load Scripts locally

1) Copy the `layouts` folder over (containing the shortcuts)
2) Copy the `static` folder (js & css)
3) Call the load shortcut in every post or globally in the theme

    {{< load-leaflet-local >}}

## Usage

### Map only

    {{< leaflet-simple mapHeight="[MAPHEIGHT]" mapWidth="[MAPWIDTH]" mapLon="[MAPLON]" mapLat="[MAPLAT]" zoom="[ZOOM]">}}

* `MAPHEIGHT` = px | %
* `MAPWIDTH` = px (must be pixels! Otherwise the map will not be shown)
* `MAPLON` = longitude where to center the map
* `MAPLAT` = latitude where to center the map
* `ZOOM` = the zoom level. This attribute is optional, default zoom level is 13. If set, it must be an int.

### Map with one marker

#### Marker _without_ Popup

**Shortcut**

    {{< leaflet-simple mapHeight="[MAPHEIGHT]" mapWidth="[MAPWIDTH]" mapLon="[MAPLON]" mapLat="[MAPLAT]" markerLon="[MARKERLON]" markerLat="[MARKERLAT]">}}


* `MAPHEIGHT` = px | %
* `MAPWIDTH` = px (must be pixels! Otherwise the map will not be shown)
* `MAPLON` = longitude where to center the map
* `MAPLAT` = latitude where to center the map
* `MARKERLON` = longitude where to place the marker
* `MARKERLAT` = latitude where to place the marker
* `ZOOM` = the zoom level. This attribute is optional, default zoom level is 13. If set, it must be an int.

#### Marker _with_ Popup

    {{< leaflet-simple mapHeight="[MAPHEIGHT]" mapWidth="[MAPWIDTH]" mapLon="[MAPLON]" mapLat="[MAPLAT]" markerLon="[MARKERLON]" markerLat="[MARKERLAT]" markerContent="[MARKERCONTENT]">}}

* `MAPHEIGHT` = px | %
* `MAPWIDTH` = px (must be pixels! Otherwise the map will not be shown)
* `MAPLON` = longitude where to center the map
* `MAPLAT` = latitude where to center the map
* `MARKERLON` = longitude where to place the marker
* `MARKERLAT` = latitude where to place the marker
* `MARKERCONTENT` = Content that should be displayed in marker popup (Can be HTML)
* `ZOOM` = the zoom level. This attribute is optional, default zoom level is 13. If set, it must be an int.

## Donate

## License

GPL v2

## Attribution

This is a fork from [simonfrey/hugo-leaflet](https://github.com/simonfrey/hugo-leaflet), which unfortunately looks abandoned.

---

*Keywords*: Open Street Map, Hugo, HugoCMS, Leaflet, Maps, Hugo Maps Plugin, Shortcut, OSM