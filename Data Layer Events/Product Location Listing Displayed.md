# Product Location Listing Displayed

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ ecommerce: null });  // Clear the previous ecommerce object.
dataLayer.push({
  "event": "view_item_list",
  "detailed_event": "Product Location Listing Displayed",
    "ecommerce": {
        "item_list_id": "<item_list_id>",
        "item_list_name": "<item_list_name>",
        "items": [
            {
                "item_id": "<item_id>",
                "item_name": "<item_name>"
            }
        ],
        "number_of_items_displayed": <number_of_items_displayed>
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|ecommerce.item_list_id|string|The computer-readable machine name of the list the item showed up in \(if sent with a view\_item\_list event\). Use UUID provided by the component if no more specific ID is available.|12345abcde12345|||||||
|ecommerce.item_list_name|string|The human-readable name of the item list the item showed up in \(if sent with a view\_item\_list event\). If one is not available, populate with numerical index of which list this is on the page \(1-indexed\). For filter\_by\_group component, use that value.|filter\_by\_group, recommended\_products, recently\_viewed\_products|||||||
|ecommerce.items[n].item_id|string|Item ID \(context-specific\).The product primary ID \(Hotel Code\)|PHXRST|||||||
|ecommerce.items[n].item_name|string|Full name of the hotel as listed on the website|Omni Scottsdale Resort & Spa at Montelucia|||||||
|ecommerce.number_of_items_displayed|integer|Captures the number of product locations displayed in a product location listing.|Ford, Chevrolet, Dodge, Levis, Columbia, Patagonia|||||||




