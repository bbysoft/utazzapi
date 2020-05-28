# Booking create

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
 price | integer *| price of booking
 payprice | integer *| payable price
 contact | array *| Array of contact objects
 rooms | array *| Array of room objects
 comment | string | booking comment

### Contact object

Field | Type | Description
---------|----------|---------
 first_name | string *| First name
 last_name | string *| Last name
 title | string | Title ( Dr. / Prof etc. )
 email | string *| E-mail
 phone | string *| Phone number, example: +36301234567

 ### Room object

Field | Type | Description
---------|----------|---------
 id | integer *| Room ID
 adultCount | integer *| Amount of adults
 childCount | integer *| Cmount of children
 children_age | string *| Ages of children (comma separated) "4,7"
 price | integer *| price of room


## Request example


```json
{
    "hotelID": 2696,
    "rate": 46009,
    "curr": "HUF",
    "start": "2020-06-06",
    "end": "2020-06-08",
    "nights": 2,
    "price": 330,
    "payprice": 330,
    "contact": {
        "first_name": "James",
        "last_name": "Bond",
        "title": "Dr.",
        "email": "007@007.com",
        "phone": "+36301234567"
    },
    "rooms": [
        {
            "id": 6104,
            "adultCount": 2,
            "childCount": 0,
            "children_age": "",
            "price": 165
        },
        {
            "id": 6104,
            "adultCount": 2,
            "childCount": 0,
            "children_age": "",
            "price": 165
        }
    ],
    "comment": ""
}
```
## Response
### Main object

Field | Type | Description
---------|----------|---------
 message | string *| status message, value: (success / fail)
 result | object | Amount of adults

### Result object

Field | Type | Description
---------|----------|---------
 booking_code | integer *| utazzitthon booking ID
 
 ## Response example

Success
```json
{
    "message": "success",
    "result": {
        "booking_code": 42354
    }
}

```
Fail
```json
{
    "message": "fail"  
}

```
