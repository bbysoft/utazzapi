# Availbility

\* = *required*

## Request
### Main object
Field | Type | Description
---------|----------|---------
 hotelID | integer *| Hotel ID
 rate | integer *| Rate ID
 curr | string | Currency ( HUF/EUR/CZK )
 start | string *| Arrival date ( yyyy-mm-dd )
 end | string *| Departue date ( yyyy-mm-dd )
 nights | integer *| nights
 rooms | array *| Array of room objects

### Room object

Field | Type | Description
---------|----------|---------
 id | integer *| Room ID
 adultCount | integer *| Amount of adults
 childCount | integer *| Cmount of children
 children_age | string *| Ages of children (comma separated) "4,7"

## Request example


```json
{
    "hotelID": 2696,
    "rate": 54044,
    "curr": "HUF",
    "start": "2020-05-01",
    "end": "2020-05-01",
    "nights": 2,
    "rooms": [
        {
            "id": 6104,
            "adultCount": 2,
            "childCount": 0,
            "children_age": ""
        },
        {
            "id": 6104,
            "adultCount": 2,
            "childCount": 1,
            "children_age": "7"
        }
    ]
}

```
## Response
### Main object

Field | Type | Description
---------|----------|---------
 message | string *| status message, value: (available / notavailable)
 result | object | Amount of adults

### Result object

Field | Type | Description
---------|----------|---------
 price | integer *| if status available then return price
 
 ## Response example

Available
```json
{
    "message": "available",
    "result": {
        "price": 330
    }
}

```
Not available
```json
{
    "message": "notavailable"  
}

```
