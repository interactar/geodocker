#Based on repository: winsent/geoserver , thanks for starting with this. :)

## Table of contents

* [What is Geoserver](#markdown-header-What is GeoServer)
* [Setup](#markdown-header-setup)

# What is GeoServer? #
GeoServer is a Java-based software server that allows users to view and edit geospatial data. Using open standards set forth by the [Open Geospatial Consortium (OGC)](http://www.opengeospatial.org/), GeoServer allows for great flexibility in map creation and data sharing.

![GeoServer_200.png](http://static.geoserver.org/images/GeoServer_200.png)

wiki: [wikipedia.org](https://wikipedia.org/wiki/GeoServer) | site: [geoserver.org](http://geoserver.org/) | documentation: [docs.geoserver.org](http://docs.geoserver.org/) | repository: [github.com](https://github.com/geoserver/geoserver)
# Image description #

Is not official GeoServer image based on `Oracle Java` with `JAI 1.1.3`, `ImageIO 1.1`, `GDAL 1.10.1` and extensions:

* ogr
* gdal
* printing
* importer

## Setup
  1. Do a docker login
  1. Clone this repository and all sub-repositories please do: `git clone --branch development --recursive git@github.com:jailbirt/geodocker.git`

    **MacOSX IMPORTANT: All repositories MUST be cloned in Users home directory. For example: /Users/yourmacuser/theeye**

## Start

  * Run `docker-compose up` for starting: geoserverwriter / geoserverreader1 / geoserverreader2 / nginx for load balancing.
  The app should then be running on your docker daemon on port 8080 (On OS X you can use `boot2docker ip` to find out the IP address).

## Workarounds (F.A.Q)

###Logs
For easier logs read you can run:
`docker-compose up > /tmp/someArchive and then tail -f /tmp/someArchive | grep --line-buffered`

## Using a custom GeoServer data directory ##
Make geoserver data directory and run container, change its path at docker-compose.yml for mounting it.

## License ##
GeoServer licensed under the [GPL](http://www.gnu.org/licenses/old-licenses/gpl-2.0.html).

# User Feedback
