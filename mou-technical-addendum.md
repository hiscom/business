---
title: AVH MoU Technical Addendum
---
This document is an addendum to the Memorandum of Understanding for the Australasian Virtual Herbarium (AVH). It is a separate document from the MoU, so that it can be more easily updated in order to keep up with changing requirements. This document covers the technical aspects of provision of data to AVH, such as delivery mechanism, frequency of delivery and quality and completeness of the provided data. CHAH and HISCOM understand that not all herbaria will be able to meet all requirements from the moment they sign the MoU or start providing data to AVH, but we do expect that AVH providers commit to making their best effort to meet the requirements in the near future.

## Summary

* Data should be delivered as Darwin Core archives
* Data should be delivered at a minimum frequency of every three months
* All required fields must be delivered, and herbaria should actively work 
  towards delivering the fields listed as highly recommended.

## Data standard

The Australasian Virtual Herbarium is part of the Atlas of Living Australia (ALA) and therefore has to comply with the ALA data standard, which is Darwin Core, in order to fit within the ALA infrastructure. Darwin Core is the most widely used data standard for primary occurrence data as well as name data and is also used and supported by the Global Biodiversity Information Facility (GBIF).

There is a delimited text (CSV) format of Darwin Core, Darwin Core Text, that can be delivered in the form of Darwin Core Archives. A Darwin Core Archive is a ZIP file containing one or more CSV files and a small XML file that sets out the relationship between the CSV files and the meaning of the columns in the CSV files.

## Delivery mechanism and frequency

Delivery through the GBIF Internet Publishing Toolkit (IPT) is preferred, as the 
IPT validates the data against Core Types and Extensions, so is guaranteed to 
provide valid data sets that do not break the ALA ingestion pipeline.

The IPT is an Apache Tomcat application that can connect to relational database 
management systems, like MySQL and PostgreSQL, or load CSV files and publishes 
out the data as Darwin Core Archives. ALA can connect directly to IPT data 
resources. AVH Providers can set up their own IPT, which is recommended for 
Australian Commonwealth, state and territory herbaria. ALA will also make an IPT 
available for ALA data providers to use (for uploading CSV files). While tthis 
is not yet available, AVH providers can use the Royal Botanic Gardens Victoria 
IPT. New Zealand herbaria provide their data through an IPT that is hosted by 
Manaaki Whenua/Landcare Research.

It is also fairly easy to create Darwin Core Archives manually or by script. 
Some AVH providers – BRI, HO and MELU – do this.

The preferred delivery frequency is weekly, but smaller herbaria which do not 
update their data as frequently may deliver at larger and less regular intervals. 
Data in AVH should be refreshed at least once a year.

## AVH data

**AVH providers should only deliver data for specimens that are held at their own institutions, not records of images of specimens held elsewhere.**

The fields that can be delivered to AVH are listed below and are explained on 
the [HISPID website](https://hiscom.github.io/hispid/terms/). A somewhat 
outdated pages that might still be helpful while we keep improving the HISPID 
site is also available on the [HISCOM Wiki](https://hiscom.rbg.vic.gov.au/wiki/AVH_data).

There are a number of required and highly recommended fields that will be listed under the subheadings below. In order to get the most value out of AVH as both a research and curation tool it is highly recommended to deliver as many of the other fields as possible.

### Fields required for every record

* [institutionCode](https://hiscom.github.io/hispid/terms/#institutionCode)
* [collectionCode](https://hiscom.github.io/hispid/terms/#institutionCode)
* [catalogNumber](https://hiscom.github.io/hispid/terms/#catalogNumber)
* [occurrenceID](https://hiscom.github.io/hispid/terms/#occurrenceID)
* [modified](https://hiscom.github.io/hispid/terms/#modified)

### Fields required for records for which they are available or relevant

* [country](https://hiscom.github.io/hispid/terms/#country)
* [stateProvince](https://hiscom.github.io/hispid/terms/#stateProvince)
* [locality](https://hiscom.github.io/hispid/terms/#locality)
* [decimalLongitude](https://hiscom.github.io/hispid/terms/#decimalLongitude)
* [decimalLatitude](https://hiscom.github.io/hispid/terms/#decimalLatitude)
* [coordinateUncertaintyInMeters](https://hiscom.github.io/hispid/terms/#coordinateUncertaintyInMeters)
* [eventDate](https://hiscom.github.io/hispid/terms/#eventDate)
* [parentEventID](http://hiscom.rbg.vic.gov.au/hispid/terms/bushBlitzExpedition) (BushBlitz participants only)
* [identificationQualifier](https://hiscom.github.io/hispid/terms/#identificationQualifier)
* [identifiedBy](https://hiscom.github.io/hispid/terms/#identifiedBy)
* [identificationDate](https://hiscom.github.io/hispid/terms/#identificationDate)
* [typeStatus](https://hiscom.github.io/hispid/terms/#typeStatus)
* [scientificName](https://hiscom.github.io/hispid/terms/#scientificName)
* [taxonRank](https://hiscom.github.io/hispid/terms/#taxonRank)
* [family](https://hiscom.github.io/hispid/terms/#family)
* [genus](https://hiscom.github.io/hispid/terms/#genus)
* [specificEpithet](https://hiscom.github.io/hispid/terms/#specificEpithet)
* [infraspecificEpithet](https://hiscom.github.io/hispid/terms/#infraspecificEpithet)

### Highly recommended fields

* [recordedBy](https://hiscom.github.io/hispid/terms/#recordedBy)
* [recordNumber](https://hiscom.github.io/hispid/terms/#recordNumber)
* [eventRemarks](https://hiscom.github.io/hispid/terms/#eventRemarks)
* [georeferencedBy](https://hiscom.github.io/hispid/terms/#georeferencedBy)
* [georeferenceProtocol](https://hiscom.github.io/hispid/terms/#georeferenceProtocol)
* [minimumElevationInMeters](https://hiscom.github.io/hispid/terms/#minimumElevationInMeters),&nbsp;[maximumElevationinMeters](https://hiscom.github.io/hispid/terms/#maximumElevationInMeters)
* [habitat](https://hiscom.github.io/hispid/terms/#habitat)
* Higher taxonomy:&nbsp;[family](https://hiscom.github.io/hispid/terms/#family),&nbsp;[order](https://hiscom.github.io/hispid/terms/#order),&nbsp;[class](https://hiscom.github.io/hispid/terms/#class),&nbsp;[phylum](https://hiscom.github.io/hispid/terms/#phylum),&nbsp;[kingdom](https://hiscom.github.io/hispid/terms/#kingdom)
* [identificationRemarks](https://hiscom.github.io/hispid/terms/#identificationRemarks)
