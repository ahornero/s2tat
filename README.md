<img align="right" src="https://raw.githubusercontent.com/ahornero/s2tat/master/favicon.png">

![Sentinel-2 Tools and Tips](https://img.shields.io/badge/Sentinel--2-Tools%20and%20Tips-green.svg)
[![Licence](https://img.shields.io/badge/license-GPLv3-orange.svg)](http://www.gnu.org/licenses/gpl-3.0.html)

# Sentinel-2 Tools and Tips

## Sen2cor
### Sen2cor 2.3.1 processing error
Just downgrade the numpy version, and it works.
```sh
$ pip install numpy==1.11.3
```
### Execution example
```sh
$ L2A_Process S2A_OPER_PRD_MSIL1C_PDMC_20160626T150256_R136_V20160626T093744_20160626T093744.SAFE
```
### Execution example with elapsed time
[elapsed_time.sh](https://github.com/ahornero/s2tat/blob/master/elapsed_time.sh) and [elapsed_time.bat](https://github.com/ahornero/s2tat/blob/master/elapsed_time.bat)

## GDAL
### .jp2 and [Sentinel-2 driver](http://www.gdal.org/frmt_sentinel2.html) compatibility
Upgrade to GDAL 2.2 (available from GDAL >= 2.1.3)
```sh
$ conda install -c conda-forge gdal=2.2.0
```
### GDAL with S2
Examples and documentation: [Driver for Sentinel-2 products](http://www.gdal.org/frmt_sentinel2.html) downloaded from [the Sentinels Scientific Data Hub](https://scihub.copernicus.eu/).

## Sentinelsat
A very [usefull tool](https://github.com/ibamacsr/sentinelsat) to find and download Copernicus Sentinel satellite images.
### Installation
```sh
$ pip install sentinelsat
```
### Usage
```sh
$ sentinel search --sentinel2 --md5 --cloud 10 -s 20160620 -e 20160630 <username> <password> <your-map>.geojson
```
GeoJSON Map tool: [geojson.io](http://geojson.io)
