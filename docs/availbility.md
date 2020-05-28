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
    "hotelID": 2696,
    "rate": 46009,
    "curr": "HUF",
    "start": "2020-06-06",
    "end": "2020-06-08",
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

