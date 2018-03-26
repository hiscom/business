This document is an addendum to the Memorandum of Understanding for the Australasian Virtual Herbarium (AVH). It is a separate document from the MoU, so that it can be more easily updated in order to keep up with changing requirements. This document covers the technical aspects of provision of data to AVH, such as delivery mechanism, frequency of delivery and quality and completeness of the provided data. CHAH and HISCOM understand that not all herbaria will be able to meet all requirements from the moment they sign the MoU or start providing data to AVH, but we do expect that AVH providers commit to making their best effort to meet the requirements in the near future.

## Summary

* Data should preferably be delivered via a BioCASe provider or as Darwin Core archives
* Data must be updated at a minimum frequency of every three months
* Data must be re-indexed at least yearly
* All required fields must be delivered, and herbaria should actively work towards delivering the fields listed as highly recommended.


## Data standard

The Australasian Virtual Herbarium is part of the Atlas of Living Australia (ALA) and therefore has to comply with the ALA data standard, which is Darwin Core, in order to fit within the ALA infrastructure. Darwin Core is the most widely used data standard for primary occurrence data as well as name data and is also used and supported by the Global Biodiversity Information Facility (GBIF).

The vehicle that is used by most Australian herbaria is ABCD, which is a form of XML. There is also a delimited text (CSV) format, Darwin Core Text, available, that can be delivered in the form of Darwin Core Archives. A Darwin Core Archive is a ZIP file containing one or more CSV files and a small XML file that sets out the relationship between the CSV files and the meaning of the columns in the CSV files. Darwin Core Archives are used to forward the aggregated AVH data to AVH. When the New Zealand herbaria join AVH, they will most likely deliver directly in Darwin Core Text. This option is also available to Australian herbaria.

## Delivery mechanism

All current AVH providers use a BioCASe provider to provide data to AVH. The BioCASe provider gets data from a database and can turn it into various forms of XML, including ABCD, HISPID and Darwin Core. As the BioCASe provider can be queried, it is possible to harvest just the updated records, as you can just query for records that have been updated since the last harvest. In order to be harvested, the BioCASe provider requires an open HTTP port all the time and hence may not be an option for every AVH provider. Also, while installing the BioCASe software and mapping a database to ABCD in HISPID in BioCASe is easy, creating the database from which the BioCASe provider can consume data may, depending on the structure of the collections database, be very hard.

Another provider that is available is the GBIF Internet Publishing Toolkit (IPT). The IPT can dump database tables and views into a Darwin Core Archive. There is much less mapping involved in the IPT: the fields in the underlying tables or views have to be the same as those of the CSV files in the Darwin Core Archive. The IPT doesn’t allow querying, so can’t be used to deliver only updated records (unless the underlying database tables or views only contain updated records). However, as the IPT does much less work than the BioCASe provider, performance should be better and the output will be compressed (and IPT output is already much smaller than XML files produced by BioCASe providers), so the files won’t be huge. Therefore it might still be an option for infrequent delivery.

HISCOM realises that, especially for smaller herbaria, neither delivery method might be feasible and we will work together with any herbarium that wants to deliver data to AVH – and can fulfill the requirements of the MoU – to get their data into AVH. Herbaria that want to join AVH should contact the HISCOM Technical Coordinator for technical advice.

## Delivery frequency

Dynamic delivery of data via a BioCASe provider, which will be harvested weekly, is preferred. For periodical delivery, delivery frequency should be at least every three months. Herbarium data sets need to be re-indexed,&nbsp;''i.e.''&nbsp;re-delivered and re-uploaded, once a year. Re-indexing can be done via a BioCASe archive or Darwin Core Archive, depending on your delivery method.

## AVH data

**AVH providers should only deliver data for specimens that are held at their own institutions, not records of images of specimens held elsewhere.**

The fields that can be delivered to AVH are listed and explained on the&nbsp;[http://hiscom.rbg.vic.gov.au/wiki/AVH_data AVH data]&nbsp;page ([http://hiscom.chah.org.au/wiki/AVH_data http://hiscom.chah.org.au/wiki/AVH_data]) on the HISCOM Wiki. There are a number of required and highly recommended fields that will be listed under the subheadings below. In order to get the most value out of AVH as both a research and curation tool it is highly recommended to deliver as many of the other fields as possible.

### Fields required for every record

* [institutionCode](http://hiscom.rbg.vic.gov.au/avhfields/institutionCode)
* [collectionCode](http://hiscom.rbg.vic.gov.au/avhfields/institutionCode)
* [catalogNumber](http://hiscom.rbg.vic.gov.au/avhfields/catalogNumber)
* [occurrenceID](http://hiscom.rbg.vic.gov.au/avhfields/occurrenceID)
* [modified](http://hiscom.rbg.vic.gov.au/avhfields/modified)

### Fields required for records for which they are available or relevant

* [country](http://hiscom.rbg.vic.gov.au/avhfields/country)
* [stateProvince](http://hiscom.rbg.vic.gov.au/avhfields/stateProvince)
* [locality](http://hiscom.rbg.vic.gov.au/avhfields/locality)
* [decimalLongitude](http://hiscom.rbg.vic.gov.au/avhfields/decimalLongitude)
* [decimalLatitude](http://hiscom.rbg.vic.gov.au/avhfields/decimalLatitude)
* [coordinateUncertaintyInMeters](http://hiscom.rbg.vic.gov.au/avhfields/coordinateUncertaintyInMeters)
* [eventDate](http://hiscom.rbg.vic.gov.au/avhfields/eventDate)
* [bushBlitzExpedition](http://hiscom.rbg.vic.gov.au/hispid/terms/bushBlitzExpedition) (BushBlitz participants only)
* [identificationQualifier](http://hiscom.rbg.vic.gov.au/avhfields/identificationQualifier)
* [identifiedBy](http://hiscom.rbg.vic.gov.au/avhfields/identifiedBy)
* [identificationDate](http://hiscom.rbg.vic.gov.au/avhfields/identificationDate)
* [typeStatus](http://hiscom.rbg.vic.gov.au/avhfields/typeStatus) (including [typifiedName](http://rs.tdwg.org/ontology/voc/Specimen#typeForName))
* [scientificName](http://hiscom.rbg.vic.gov.au/avhfields/scientificName)
* [taxonRank](http://hiscom.rbg.vic.gov.au/avhfields/taxonRank)
* [family](http://hiscom.rbg.vic.gov.au/avhfields/family)
* [genus](http://hiscom.rbg.vic.gov.au/avhfields/genus)
* [specificEpithet](http://hiscom.rbg.vic.gov.au/avhfields/specificEpithet)
* [infraspecificEpithet](http://hiscom.rbg.vic.gov.au/avhfields/infraspecificEpithet)



### Highly recommended fields

* [recordedBy](http://hiscom.rbg.vic.gov.au/avhfields/recordedBy)
* [recordNumber](http://hiscom.rbg.vic.gov.au/avhfields/recordNumber)
* [eventRemarks](http://hiscom.rbg.vic.gov.au/avhfields/eventRemarks)
* [georeferencedBy](http://hiscom.rbg.vic.gov.au/avhfields/georeferencedBy)
* [georeferenceProtocol](http://hiscom.rbg.vic.gov.au/avhfields/georeferenceProtocol)
* [minimumElevationInMeters](http://hiscom.rbg.vic.gov.au/avhfields/minimumElevationInMeters),&nbsp;[maximumElevationinMeters](http://hiscom.rbg.vic.gov.au/avhfields/maximumElevationInMeters)
* [habitat](http://hiscom.rbg.vic.gov.au/avhfields/habitat)
* Higher taxonomy:&nbsp;[order](http://hiscom.rbg.vic.gov.au/wiki/AVH_data#order),&nbsp;[class](http://hiscom.rbg.vic.gov.au/wiki/AVH_data#class),&nbsp;[phylum](http://hiscom.rbg.vic.gov.au/wiki/AVH_data#phylum),&nbsp;[kingdom](http://hiscom.rbg.vic.gov.au/wiki/AVH_data#kingdom)
* [identificationRemarks](http://hiscom.rbg.vic.gov.au/avhfields/identificationRemarks)
