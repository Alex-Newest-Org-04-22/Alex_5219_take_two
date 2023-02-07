# Add Add-on

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ ecommerce: null });  // Clear the previous ecommerce object.
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "add_addon",
  "detailed_event": "Add Add-on",
    "ecommerce": {
        "items": [
            {
                "item_id": "<item_id>"
            }
        ]
    },
    "event_data": {
        "addon_name": "<addon_name>",
        "addon_price": <addon_price>
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|ecommerce.items[n].item_id|string|Item ID \(context-specific\).The product primary ID \(Hotel Code\)|PHXRST|||||||
|event_data.addon_name|string|Name of add-on being added to hotel bookings|CHAMPAGNE & ARTISANAL CHOCOLATES, $200 DINING CREDIT FOR $180|||||||
|event_data.addon_price|number|Price of each add-on added to a hotel booking||||||||

## Attached Notes

<p>this event fires on the Customize your Stay screen when users add an amenity to their booking such as Dining Credit, Late Checkout, etc. It will capture both the amenity name and the amenity price (per add amenity event)</p>
