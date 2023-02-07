# Social Brand Followed

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "subscribe_social",
  "detailed_event": "Social Brand Followed",
    "event_data": {
        "method": "<method>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.method|string|Captures the name of the social network associated with social network activity \(i.e. follow, share\).|facebook, linkedIn, instrgram, twitter|||||||

## Attached Notes

<p>This is for when a user clicks an outbound link to one of the social properties such as Youtube, Facebook, etc.</p>
