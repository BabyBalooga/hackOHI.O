# HackOHI.O
Data For OSU Hackathon

There are two files, data and config, linked on the column MeterID.

------
--- HackathonData.csv
------
The data file contains time series data for the challenge. Each meter represents the consumption for one of the following resources: Chilled Water, Heating Hot Water, or Steam. Each meter has two years (or less in some cases) of average daily usage.
|Field Name | Field Description|
|---------- | -----------------|
|MeterID|              Meter identifier, will have a match in the config file|
|CurrentValue|         Most precise measurement value|
|ValueString|          Less precise measurement value|
|Time|                 Time of measurement in UTC, format yyyy-mm-ddThh:mm:ssZ|
|Status|               Sometimes meters malfunction. Indicator for if this time period of data is OK or UNRELIABLE|
|StatusCode|           Numeric representation of status|


------
--- HackathonConfig.csv
------
The config file contains meta data for the challenge. Each meter represents consumption for a building. Meter and building attributes are included here.
                      
* MeterID:              Meter identifier, will have a match in the config file
* Description:          Description of what the meter is measuring
* Units:                Unit of measurement for this meter
* Resource:             Resource measured by this meter, can be Chilled Water, Heating Hot Water, or Steam
* BuildingID            ID for the building where this meter is located
* BuildingName          Name for this building
* GrossSquareFeet       Size of this building in square feet
* BuildDate             Construction date of this building
* Latitude              Latitude coordinate for this building
* Longitude             Longitude coordinate for this building
* Campus:               Can be Main or Medical Center
* Organization:         Organization which manages this building
* LocationType:         Category of usage for this building
* SteamSourceID:        BuildingID representing the source of steam for this building (1)
* ChilledWaterSourceID: BuildingID representing the source of chilled water for this building (1)
* otWaterSourceID:     BuildingID representing the source of hot water for this building (1)

1 Some buildings are supplied by other buildings on campus and will have values, others are supplied by external sourced and will not have values.
