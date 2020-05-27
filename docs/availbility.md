# availbility


Field | Type | Description
---------|----------|---------
 hotelID | integer | Hotel ID
 rate | integer | Rate ID
 curr | string | Currency ( HUF/EUR/CZK )
 start | string | Arrival date ( yyyy-mm-dd )
 end | string | Departue date ( yyyy-mm-dd )
 nights | integer | nights
 rooms | array | Array of room objects

```json
{
    "hotelID":289,
    "rate": 51689,
    "curr": "HUF",
    "start": "2020-06-14",
    "end": "2020-06-16",
    "nights": 2,
    "rooms":[
        {
        "id": 4553,
        "adultCount": 2,
        "childCount": 0,
        "children_age": ""
        },
        {
        "id": 4553,
        "adultCount": 2,
        "childCount": 2,
        "children_age": "4,7"
        }
    ]
}

```