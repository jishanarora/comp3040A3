# Manitoba Provincial Parks

### API Description
A simple API to provide some general information about the Manitoba Provincial Parks. Users can get a list of all the provincial parks in Manitoba, or get information about a specific park they might want to visit.

### Endpoints
There is one endpoint at _api.parkfinder.org/json_. Using different parameters allows the user to either get a list of parks in Manitoba, or get information about a specific park by name or by location.

### Parameters
There are three parameters.
1. name(string): Default is "". Required.
>- The name of a specific park. 
>- If "", all provincial parks names will be returned.
>- If specified, parks with the same name will be returned.
2. postalcode: Default is "". Optional.
>- The postal code of a specific location. 
>- If "", other parameters will be parsed. 
>- If specified, a list of parks near the location wil be returned.
3. Fee: Default is "". Optional.
>- The fee of a specific location. 
>- If "", other parameters will be parsed. 
>- If specified, a list of parks whose fees is below or equal to the specified fees will be returned.

### Resources
#### Name parameter is "", List all parks.
```
{
  "Parks": ["park1", "park2", "park3", ...]
}
```

#### Name parameter is "Park name", return information about a specific park.
```
{
  "Name": "park name",
  "Entry Fee": 3.00,
  "Opens At": 8:00,
  "Closes At": 20:00
}
```

### Sample Requests and Responses
https://api.parkfinder.org/json?name=Birds-Hill
```
 
 {
  "Name": "Birds Hill Provincial Park",
  "Entry Fee": 8.00,
  "Opens At": 7:00,
  "Closes At": 23:00, 
 }
 ```
 https://api.parkfinder.org/json?postalcode=R0E0K0
 ```
 {
  "Name": "Birds Hill Provincial Park",
  "Entry Fee": 8.00
  "Opens At": 7:00,
  "Closes At": 23:00, 
 }
 ```
 https://api.parkfinder.org/json?name
 ```
 {
  ["Name": "Birds Hill Provincial Park",
  "Name": "Beaudry Provincial Park",
  ......,
  ......]
 }
 ```
 https://api.parkfinder.org/json?name=Birds-Hill&postalcode=R0E0K0&
 ```
 {
 []
 }
  
```
