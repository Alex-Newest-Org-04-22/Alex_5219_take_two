# Listing Filter Removed

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({
  "event": "filter_remove",
  "detailed_event": "Listing Filter Removed",
    "ecommerce": {
        "facets": "<facets>",
        "type": "<type>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|ecommerce.facets|string|Details filters used to refine a listing|sort\~price ascending\|bed type\~2PlusBeds\|room type\~poolside|||||||
|ecommerce.type|string|Captures the methods that bring users to listings \(i.e. Onsite Search, Top Nav, External Link, Category Landing Page\). Does not update if listings are sorted, filtered, or paginated.|Product, Location, Event, Room, Content|||||||

## Attached Notes

<p>This is used for the filter on the hotel rooms listing page.</p>
