# Natura2000 example

## Introduction
This is a example implementation of our [Docker base image](https://github.com/PDOK/mapserver-wfs-gpkg). It contains a mapfile natura2000.map and a geopackage natura2000.gpkg containing the vector data.

## Usage
```
git clone https://github.com/PDOK/mapserver-wfs-gpkg.git
cd /mapserver-wfs-gpkg
git checkout natura2000-example
```

```
docker build -t natura2000-example .
```

```
docker run -d -p 80:80 --name natura2000-service natura2000-example
```

Check if it works: http://localhost/natura2000/wfs?request=getcapabilities&service=wfs&version=2.0.0 should return an getcapabilities document.

![getcapabilities](/img/getcapabilities-natura2000.jpg)
