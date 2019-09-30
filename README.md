# Geopackage Optimizer

This utility uses [NGA's Geopackage Optimizer](https://github.com/ngageoint/geopackage-js/tree/master/optimizer) in order to pre-optimize Geopackages for use on the web (MAGE).

## Setup

### Prerequisites

You will need to have a somewhat recent version of Node.js installed; you can download and install the appropriate version for your operating system, [from the official download page](https://nodejs.org/en/download/).

## Getting the Utility

1. [download this utility, as a ZIP file](https://github.com/TeslaGov/gpkg-optimizer/archive/master.zip)
2. extract the ZIP to a location of your choosing
3. move to the location where you extracted the zip
4. run `npm i` to install the required dependencies

## Usage

Pre-process _every_ geopackage before you upload it using the instructions below.

1. open a terminal and navigate to the location where you extracted the ZIP
2. execute the `optimize` script, giving two arguments: the input GPKG path and the output GPKG path

```bash
./optimize '<input_gpkg_path>' '<output_gpkg_path>'
```

3. this may take a lot of time depending on the complexity of the Geopackage you are processing -- be patient
4. once complete, locate the output GPKG and use this when uploading a new layer within MAGE

### Example

Given:
- you have extracted the ZIP to `/opt/gpkg-optimizer`
- you have a Geopackage you'd like to process and it is stored at `/home/my_geopackage.gpkg`

Execute the following commands within your terminal:

1. move to the location where you extracted the zip: `cd /opt/gpkg-optimizer`
2. optimize the Geopackage: `./optimize '/home/my_geopackage.gpkg' '/home/my_geopackage_optimized.gpkg'`
3. upload `/home/my_geopackage_optimized.gpkg` to MAGE
