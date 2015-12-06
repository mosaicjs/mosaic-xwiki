# Mosaic XWiki Back-Office

Mosaic XWiki is an XWiki application providing a back-office API and UI to collaborative maps such as [techonmap-v2](https://github.com/ubimix/techonmap-ui).

## Build

Requirements:
- Maven 3
- Java Development Kit 7

The command below produces a XAR file named 'mosaic-xwiki-documents.xar':

```mvn clean install```

## Installation

Requirements:
- XWiki 7.2 or above
- PostgreSQL (recommended) or MySQL
- Admin and programmation rights on XWiki

Installation steps:
- Import the XAR 'mosaic-xwiki-documents.xar' into XWiki (see above) from the Import section of the XWiki Administration page
- Re-saving the imported documents by using an account having programming rights may be needed for the scripts to execute properly

Import GeoJSON data:
- Navigate to the page ```mosaic.Importer```: http://{server-name}/xwiki/bin/view/mosaic/Importer
- Attach a GeoJSON file to that page, named ```data.geojson```
- Add ```op=import``` to the URL for launching the import: http://{server-name}/xwiki/bin/view/mosaic/Importer?op=import
- Navigate to the page ```wiki.WebHome```: all the imported organizations should show up in a table

## Roadmap

- Provide the necessary libraries for geocoding addresses from the back-office

## License

This application is available under the license LGPL v2.0.
