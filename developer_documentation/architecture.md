# PlanetServer architecture Developer guide

# Author
Ramiro Marco Figuera

# Change Log

|Version|Name|Note|
|---|---|---|
|1|Ramiro Marco Figuera|First created in Jan. 2018|

# Introduction

PlanetServer's main architecture is divided in two sides: the server and the client side. On the server side we use Rasdaman as our array database manager and WMS server. On the client side we use WebWorldWind in order to access and deploy the data. All data is accessed using the OGC standard Web Coverage Processing Service (WCPS) allowing the user to fully analyze datacubes.

# Server side

The server side contains different services. All services need to be installed and configured as mentioned in the following guides:

1. [Rasdaman](https://github.com/planetserver/ps2-documentation/blob/master/developer_documentation/rasdaman_install.md)
2. [Ports TOMCAT](https://github.com/planetserver/ps2-documentation/blob/master/developer_documentation/ports_tomcat.md)
3. [Geoserver](https://github.com/planetserver/ps2-documentation/blob/master/developer_documentation/geoserver.md)
4. [SECORE](https://github.com/planetserver/ps2-documentation/blob/master/developer_documentation/secore.md)

# Client side

The client side only contains WebWorldWind which needs to be deployed and configured as mentioned in the guideline:

1. [WebWorldWind](https://github.com/planetserver/ps2-documentation/blob/master/developer_documentation/web_world_wind_devel_guide.md)
2. Once both sides are deployed we need to initialize the python server in **/html/python/** used to stretch the colour of the images. This is done by running `nohup python start.py &`