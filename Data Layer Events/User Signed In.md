# User Signed In

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "login",
  "detailed_event": "User Signed In",
    "event_data": {
        "loyalty_points": "<loyalty_points>",
        "loyalty_status": "<loyalty_status>"
    },
    "user_data": {
        "user_id": "<user_id>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.loyalty_points|string|Captures the total loyalty points the user had at the time of the visit.||||||||
|event_data.loyalty_status|string|Captures the current loyalty status of the user.|Gold, Bronze, Platinum, Diamond, Silver|||||||
|user_data.user_id|string|Captures the loyalty ID associated with each user.|abc1234, def876, 87987659|||||||

## Attached Notes

<p>This fires when a user signs into their Omni account on the confirm your stay screen (and elsewhere)</p>
