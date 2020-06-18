# Metadata-for-problem-set-4
This is the surface weather observations hourly data from the U.S. This data was obtained from https://data.nodc.noaa.gov/cgi-bin/iso?id=gov.noaa.ncdc:C01106

| Column Name | Description |
| --- | --- |
| STATION | Unique number to identify each station for different locations |
| STATION_NAME | Name to identify each station (can be numerical or code name) |
| ELEVATION | Elevation of either rain, snow, hail in meters for recording |
| LONGITUDE | Longitude of location during time of recording/ geographic |
| LATITUDE | Latitude of location during time of recording/ geographic |
| DATE | Month (2 digits)/ day of the month/ Year (4 digits) of the time the data was recorded |

How I would normalize
In order to normalize, I would use two seperate tables. My first table would include the geographical location inportant to where the data was obtained from. This would include the following columns; 'STATION', 'STATION_NAME', 'LONGITUDE' and 'LATITUDE'.
This will allow for a more clear concise depiction of where the data came from.
The second would include the specifications by using columns; 'ELEVATION' and 'DATE'. Viewers will be able to know when the data was most relevant in accordance to the type of weather they had. The primary key for the table is 'DATE' but add in hours and seconds to prevemt overlap with perhaps another station recording at the same time. All of the other columns would likely be repeated more often.

Data Types for each column
| Column | Type |
| --- | --- |
| STATION | CHAR STRING (6 DIGITS) |
| STATION_NAME | VARCHAR STRING (max 200 characters) |
| ELEVATION |  VARCHAR STRING (max 10 characters)  |
| LONGITUDE |  VARCHAR STRING (max 10 characters) |
| LATITUDE |  VARCHAR STRING (max 10 characters) |
| DATE |  DATE+TIME |
