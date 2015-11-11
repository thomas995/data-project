## Data Representation and Querying Project 2015 
## Thomas McNamara

## Introduction 

This API will show the details on the Garda stations in the Fingal County Council. 

## About the data
This dataset was received in Comma Separated Values (CSV) format, and was downloaded from [*Garda Stations*](https://data.gov.ie/dataset/garda-stations).
The CSV file contains 19 rows, the first being a header row with the names of each field.
There are fifteen values on each line, which are as follows: 

Field | Description
------------ | -------------
Name | the name of the garda station
Address1 | The first address for the garda station.
Address2 |The second address for the garda station.
Address3 |  The third address for the garda station.
Phone | the phone number for the garda station.
Website | the website that a user can access to get information on the station.
Divison | Where the garda divison is located
Divison HQ | Which divison the garda station belongs to.
Divisonal HQ Phone | Phone number for the specific divison phone number.
District | Which district the station belongs to
District HQ | the location of the headquarters for the district the station is in. 
District HQ Phone | the phone number for the HQ of the stations.
Opening Hours | The hours the police station is open to the public for.
Lat | the latitude of where the station is.
Long | the longitude of where the station is.

## JSON version of the file for the Garda Stations
```JSON
[
{
   "Name" : "Skerries", 
   "Address1": "Strand Street",
   "Address2": "Skerries",
   "Address3": "Co.Dublin",
   "Phone": "+353 1 8491211",
   "Website": "http://www.garda.ie/Stations/Default.aspx",
   "Divison": "Dublin Metropolitan Region Northern Division",
   "Divisonal HQ": "Ballymun",
   "Divisonal HQ Phone": "+353 1 6664493",
   "District": "Balbriggan",
   "District HQ": "Balbriggan",
   "District HQ Phone": "+353 1 8020510",
   "Opening Hours": "Closes at 9pm",
   "Lat": "53.5795903768001",
   "Long": "6.1069616104728",
}
]
``` 
## Accessing certain parts of the files using HTTP and JSON
Using the websites URL will bring you to the page and show you all the information. By using keywords after the ".com" in the URL, you can list out the Name of the Garda Station in Fingal. It looks something like this: 
*http://GardaStationsAPI.com/Fingal/Name*

County | Name
------------ | -------------
Fingal | Balbriggan Garda Station
Fingal | Skerries
Fingal | Lusk Garda Station
=> And so on until all the stations from *Fingal* have had their *name* displayed. If only Fingal was put into the URL then all the data for Fingal would be outputted. 
If you wanted to output data from two different tables, such as Phone and Name, you would have the URL as: *http://GardaStationsAPI.com/Fingal/Name+PhoneNumber*

County | Name | Phone Number
------------ | ------------- | -------------
Fingal | Balbriggan Garda Station | +353 1 8020510
Fingal | Skerries | +353 1 8491211
Fingal | Lusk Garda Station | +353 1 8437222



