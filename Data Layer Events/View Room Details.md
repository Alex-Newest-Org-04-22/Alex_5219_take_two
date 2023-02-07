# View Room Details

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ ecommerce: null });  // Clear the previous ecommerce object.
dataLayer.push({
  "event": "view_details",
  "detailed_event": "View Room Details",
    "ecommerce": {
        "items": [
            {
                "item_category2": "<item_category2>",
                "item_id": "<item_id>"
            }
        ]
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|ecommerce.items[n].item_category2|string|The Room Type Code|DK|||||||
|ecommerce.items[n].item_id|string|Item ID \(context-specific\).The product primary ID \(Hotel Code\)|PHXRST|||||||

## Attached Notes

<p>This is for when a user expands room details on the Choose Room screen</p>
