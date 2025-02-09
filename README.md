# GeoKMLer

GeoKMLer is a JavaScript library designed to convert KML data into GeoJSON format efficiently. It supports the conversion of various KML geometries and extended data, making it ideal for integrating KML spatial data into web mapping applications.

## License

This project is free software licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Overview

GeoKMLer provides a straightforward API to parse KML files and convert them into a GeoJSON FeatureCollection. It is suitable for use in geographic data visualization and web mapping applications.

## Features

- **Convert KML to GeoJSON**: Supports points, linestrings, polygons, and multigeometries.
- **Handle Extended Data**: Converts KML `<ExtendedData>` elements into GeoJSON properties.
- **Robust XML Handling**: Efficient parsing and normalization of XML data.
- **No External Dependencies**: Lightweight and easy to integrate into various projects.

## Usage

To use GeoKMLer, create an instance of `GeoKMLer` and use its methods to perform conversions from KML strings to GeoJSON objects.

### Example

```javascript
var geoKMLer = new GeoKMLer(); // Create a new instance of GeoKMLer

// Sample KML data input
const kmlData = `...KML data string...`;

// Parse the KML data
const xmlDoc = geoKMLer.read(kmlData);

// Convert to GeoJSON
const geoJson = geoKMLer.toGeoJSON(xmlDoc);

console.log(geoJson);
```

## Key Methods

- read(kmlText): Parses a KML string into an XML Document using DOMParser.
- toGeoJSON(document): Converts an XML Document into a GeoJSON FeatureCollection.
- extractExtendedData(placemark): Extracts extended data from a KML Placemark and includes it as GeoJSON properties.

## Acknowledgments

The structure and logic for this project are based on established methods for XML to GeoJSON conversion, leveraging modern JavaScript best practices.

## Project Home

https://github.com/YourUsername/GeoKMLer
