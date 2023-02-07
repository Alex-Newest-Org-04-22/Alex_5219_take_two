# Room Unavailable Displayed

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "room_unavailable_displayed",
  "detailed_event": "Room Unavailable Displayed",
    "event_data": {
        "hotel_code": "<hotel_code>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.hotel_code|string|Hotel Code|PHXRST|||||||




