# Manitoba Provincial Parks

### API Description
A simple API to provide some general information about the Manitoba Provincial Parks. Users can get a list of all the provincial parks in Manitoba, or get information about a specific park they might want to visit.

### Endpoints
#### List All Parks
The user can get a list of all the provincial parks in Manitoba, as well as the total number of provincial parks. There possible parameters are name, location and fee.

#### Park Information
The user can get information about a specific provincial park using this request. Some of the information returned includes:
- Entry Fee
- Park Hours
- Location
This request requires the user to enter the name of the park as a parameter.

#### Nearest Park
The user can see what the closest provincial park to their location is. This request will return the name of the nearest park as well as its location. This request requires the user to enter their current location in longitude and latitude as a parameter.

### Resources
#### List All Parks Resources
```
{
  "Parks": ["park1", "park2", "park3", ...]
}
```

#### Park Information
```
{
  "Name": "park name",
  "Entry Fee": 3.00,
  "Hour Open": 8:00,
  "Hour Closed": 20:00,
  "Longitude": -------,
  "Latitude": -------
}
```
#### Nearest Park
```
{
  "Name": "park name",
  "Longitude": -------,
  "Latitude": -------
}
```

### Sample Request and Response
```
https://api.parkfinder.org/json?name=Birds-Hill
 
{
  "Name": "Birds Hill Provincial Park",
  "Entry Fee": 0.00,
  "Hour Open": 7:00,
  "Hour Closed": 23:00, 
  "Longitude": 50.0276° N,
  "Latitude": 96.8870° W
  }
```
