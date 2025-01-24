Dataset: Sustainable Development Goal 11
Release date: 2024-02
Data extracted on: 2024-02-16 11:52:42

- [Introduction](#introduction)
- [Intended Audience](#intended-audience)
- [Contact information](#contact-information)
- [Archive Content](#archive-content)
- [Data Model](#data-model)
- [Metadata](#metadata)
- [License](#license)
- [CHANGELOG all annotated changes for previous year](#changelog-all-annotated-changes-for-previous-year)

# Introduction
This archive consists of the latest official data disseminated by the UNESCO Institute of Statistics (UIS) for a specific dataset. This dataset was compiled using the latest data as of the date appearing at the beginning of this file. The UIS periodically updates this dataset. To find out when the next update will occur please visit http://uis.unesco.org.

# Intended Audience 
This archive is a result of a rigorous data production activity that ensures a high level of data quality. In order to expose the dataset to the largest audience possible and reduce its complexity the UIS has normalized and compiled it using comma-separated values (CSV) format. Please note all files utilize UTF-8 encoding. This allows both beginners and seasoned data professionals to understand and work with it.

More information about this data and tutorials can be found on the UIS Developer Portal here: https://apiportal.uis.unesco.org/

# Contact information
If you have any questions or comments about this archive please contact us at:

UNESCO Institute for Statistics
3500 De Maisonneuve Boulevard West, RS-1100
Montreal, Quebec, Canada H3Z 3C1
Tel: +1 514 343 6880
Email: uis.datarequests@unesco.org

# Archive Content
This archive contains the following files:

## DATASET_README_RELEASE_YEAR_Month.md
The README filename is composed of:  The abbreviation for the dataset as a prefix, and the year and month of the release as a suffix.

The README file also incorporates a header at the beginning of the file which identifies: the full title of the dataset contained in the archive, the month and year that the data was released by the UIS, and the date that the data was extracted to create the archive. The README file also details the contents of each file in the archive, as well as the data component layout and schema.  The README file is in MARKDOWN format (https://www.markdownguide.org/).

## DATASETNAME_LABEL.csv
This file is a list of all indicator codes and their descriptive labels:
|Field Name|Field Description|
|--|--|
|INDICATOR_ID |Indicator code|
|INDICATOR_LABEL_EN|Indicator code English label|

## DATASETNAME_DATA_NATIONAL.csv
This file contains all the national data available for this dataset and includes the following fields: 
|Field Name|Field Description|
|--|--|
|INDICATOR_ID|Indicator code|
|COUNTRY_ID|ISO 3166-1 alpha-3 country code|
|YEAR |Year of the measured value|
|VALUE |Measured value|
|MAGNITUDE |Metadata describing the NATURE of the measured value (see metadata section below)|
|QUALIFIER|Metadata describing the QUALITY of the measured value (see metadata section below)|

## DATASETNAME_DATA_REGIONAL.csv
This file contains all the regional data available for this dataset and includes the following fields: 
|Field Name|Field Description|
|--|--|
|INDICATOR_ID|Indicator code|
|REGION_ID|ISO 3166-1 alpha-3 country code|
|YEAR |Year of the measured value|
|VALUE |Measured value|
|MAGNITUDE |Metadata describing the NATURE of the measured value (see metadata section below)|
|QUALIFIER|Metadata describing the QUALITY of the measured value (see metadata section below)|


## DATASETNAME_METADATA.csv
This file contains all the metadata associated to the NATIONAL and REGIONAL data files above and includes the following fields: 
|Field Name|Field Description|
|--|--|
|INDICATOR_ID|Indicator code|
|COUNTRY_ID|ISO 3166-1 alpha-3 country code|
|YEAR |Year of the metadata value|
|TYPE |Type of metadata|
|METADATA|Metadata value|

## DATASETNAME_COUNTRY.csv
This file lists all country codes and their descriptive labels:
|Field Name|Field Description|
|--|--|
|COUNTRY_ID|ISO 3166-1 alpha-3 country code|
|COUNTRY_NAME_EN|UNSTATS M49 STANDARD English country name (https://unstats.un.org/unsd/methodology/m49/)|

## DATASETNAME_REGION.csv
This file lists all regions and the countries that belong to each region:
|Field Name|Field Description|
|--|--|
|REGION_ID|Label is composed of the name (acronym) of the organization that is responsible for the regional composition + ': ' + name of the region
|COUNTRY_ID|ISO 3166-1 alpha-3 country code|
|COUNTRY_NAME_EN|UNSTATS M49 STANDARD English country name (https://unstats.un.org/unsd/methodology/m49/)|

# Data Model
The National (and Regional when available) data files can be linked with the: 
- **label file** using the “INDICATOR_ID” variable as the matching key.
- **metadata file** (when available) using the “INDICATOR_ID”+”COUNTRY_ID”+”YEAR” variables combined as the matching key. Be aware that multiple metadata entries can match a unique data point from the data file i.e. there can be multiple metadata rows for a specific INDICATOR_ID/COUNTRY_ID/YEAR combination. Note that there can also be multiple entries within the same INDICATOR_ID/COUNTRY_ID/YEAR/TYPE combination. 

# Metadata
## Indicator Metadata
Most indicators have a Glossary entry that can be accessed on the UIS website at http://uis.unesco.org/en/glossary containing the indicators’: definition, interpretation, purpose, quality standards, calculation, types of disaggregation and limitation.

## Magnitude
MAGNITUDE describes the NATURE of the data point. Possible values are: 
- **NIL** – The value will be 0, and should be treated as NIL.
- **NA** – The value will be 0.  This data point is NOT APPLICABLE for the submitting nation.
- **SUPP** -  The value will be BLANK.  The data point was SUPPRESSED by request of the submitting nation.
- **LOWREL** – The value will be NUMERIC.  The data point is of LOW RELIABILITY.
- **INCLUDED** – The value will be BLANK. This data is INCLUDED in ANOTHER data point.
- **INCLUDES** – The value will be NUMERIC.  This data point INCLUDES data from another data point.

## Qualifier
QUALIFIER describes the QUALITIES of the data point. Possible values are:
- **NAT_EST** – The value will be NUMERIC.  This data point is a NATIONAL ESTIMATE.
- **UIS_EST** – The value will be NUMERIC.  This data point is an ESTIMATE produced by the UNESCO INSTITUTE FOR STATISTICS.

# License
This dataset is licensed under the Creative Commons Attribution-ShareAlike 3.0 IGO License. To view a copy of this license, visit http://creativecommons.org/licenses/by-sa/3.0/igo/ or send a letter to Creative Commons, PO Box 1866, Mountain View, CA 94042, USA.

# CHANGELOG all annotated changes for previous year

