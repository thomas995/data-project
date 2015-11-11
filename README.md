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

If you wanted to output data from *two different table*s, such as *Phone* and *Name*, you would have the URL as: *http://GardaStationsAPI.com/Fingal/Name&PhoneNumber*.

County | Name | Phone Number
------------ | ------------- | -------------
Fingal | Balbriggan Garda Station | +353 1 8020510
Fingal | Skerries | +353 1 8491211
Fingal | Lusk Garda Station | +353 1 8437222
=> And so on until all the values are outputted just like the first example. You can do this with the rest of the Field values. The "&" symbol allows the user looking for the files to combine the results so that the contents of both tables are outputted.

If you wanted only a certain amount values to be outputted you can change the URL to the following:
*http://GardaStationsAPI.com/Fingal/Opening+Hours/6*.

County | Opening Hours
------------ | -------------
Fingal | Open 24hrs
Fingal | Closes at 9pm
Fingal | Closes at 9pm
Fingal | Closes at 9pm
Fingal | Open 24hrs
Fingal | Closes at 9pm

=> And stops outputting the results for the "Opening Hours" after the fourth one is shown. This can be done with all the values on the table.

## Codes that may appear in Web Page when searching the datasets:
Number | Meaning
------------ | -------------
200 | OK  
202 | Accepted 
301 | Moved Permanently
400 | Moved Temporarily
401 | Bad Request
404 | Not Found


## Result
The API is useful to all types of users. Being able to find a Garda Station is handy for a number a reasons. These includes getting an Age Card so that you have identification saying you are over the age of 18 and going to them for any problems you may have that only they can solve i.e a stolen handbag or wallet. It's also handy to be able to find them, as people who want to work around children will need to get a Garda Vetting Form in order to get employment. This is needed to prove that you do not have a criminal past or have been involved in any illegal crimes. It can also be useful for users to be able to *Post* and *Delete* information from the datasets as aspects may change such as opening times or telephone numbers changing.
