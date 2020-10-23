# CinemaRural

This Github repository contains alle technical documentation about the CollectiveAccess cataloguing tool behind the [Cinema Rural Film Database](https://cagnet.be/page/cinema-rural-filmdatabank ). 

## About

Cinema Rural is a project of the Center for Agricultural History (CAG) in Leuven (Belgium), which is part of a broader international initiative led by the European Rural History Film Association.
The project aims to record agricultural film heritage, to safeguard it and make it findable and accessible for researchers and the public. CAG wants to trace as much film heritage as possible with the theme of agriculture and rural life in Belgium and make it accessible, first through the [Cinema Rural Film Database](https://cagnet.be/page/cinema-rural-filmdatabank ), then through the database of the [European Rural History Film Association](https://ruralfilms.eu).

The repository contains the Collective Access Installation Profile for the cataloguing tool that feeds the Cinema Rural Film Database, including import and export scripts, and all information about the OAI-PMH endpoint that enables re-use of metadata from the Cinema Rural Film Database in other catalogues.

## Collective Access Installation Profile
The Cinema Rural Film Database currently uses [Collective Access 1.7.6](https://collectiveaccess.org/) (CA) as a cataloguig tool. CA uses a cataloguing profile that was developed specifically for this database: [cinema_rural.xml](https://github.com/libis/CinemaRural/blob/master/cinema_rural.xml). 

Instructions for installing a CA with an external profile are available at the [CA Wiki](https://docs.collectiveaccess.org/wiki/Installation_profile).

## CSV Import Script & Template
For the purpose of uploading data exports from other memory institutions about rural films, a CSV import script and template have been developed. The import script uses a CA-specific language and is recorded in a spreadsheet that you have to upload in CA: [CA CSV Import Script v1.0](https://github.com/libis/CinemaRural/blob/master/CA%20Import%20Script.xlsx). 

More information about the syntax used is available at the [CA Wiki](https://docs.collectiveaccess.org/wiki/Data_Importer#Overview). 

The script requires the use of the following CSV template: [CinemaRuralCsvImportTemplate](https://github.com/libis/CinemaRural/blob/master/CinemaRuralCsvImportTemplate.csv).  

## EBUCORE Export Script
For the purpose of sharing data from the Cinema Rural Film Database with other organisations, an EBUCORE export script has been developed. This export script also uses a CA-specific language and is recorded in a spreadsheet that you have to upload in CA:  [CinemaRuralEbucoreExportScript-v1.0](https://github.com/libis/CinemaRural/blob/master/CinemaRuralEbucoreExportScript-v1.0.xlsx). 

More information about the syntax used is available at the [CA Wiki](https://docs.collectiveaccess.org/wiki/Data_Exporter).

## Cinema Rural OAI-PMH Endpoint
For the purpose of enabling synchronisation of data between the Cinema Rural Film Database and other film databases, an OAI-PMH endpoint has been configured on top of the CA database. 

Documentation about the syntax of the OAI-PMH protocol is available at http://www.openarchives.org/OAI/openarchivesprotocol.html.

The base URL for the endpoint is: https://www.hetvirtueleland.be/ca_cag/service.php/OAI/ebucore_cag_film/request.

* A list of all identifiers for the records available: https://www.hetvirtueleland.be/ca_cag/service.php/OAI/ebucore_cag_film/request?verb=ListIdentifiers
* A full harvest of all records: https://www.hetvirtueleland.be/ca_cag/service.php/OAI/ebucore_cag_film/request?verb=ListRecords
* An example of a GetRecord request: https://www.hetvirtueleland.be/ca_cag/service.php/OAI/ebucore_cag_film/request?verb=GetRecord&identifier=oai:oai.cag:38790

The &metadataPrefix allow you to define the result format. Default result format is: &metadataPrefix=ebucore.
