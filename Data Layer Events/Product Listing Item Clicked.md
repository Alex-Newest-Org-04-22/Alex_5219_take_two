# Product Listing Item Clicked

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ ecommerce: null });  // Clear the previous ecommerce object.
dataLayer.push({
  "event": "select_item",
  "detailed_event": "Product Listing Item Clicked",
    "ecommerce": {
        "item_list_id": "<item_list_id>",
        "item_list_name": "<item_list_name>",
        "items": [
            {
                "item_brand": "<item_brand>",
                "item_category": "<item_category>",
                "item_category2": "<item_category2>",
                "item_category3": "<item_category3>",
                "item_category4": <item_category4>,
                "item_category5": <item_category5>,
                "item_id": "<item_id>",
                "item_name": "<item_name>",
                "item_variant": <item_variant>
            }
        ]
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|ecommerce.item_list_id|string|The computer-readable machine name of the list the item showed up in \(if sent with a view\_item\_list event\). Use UUID provided by the component if no more specific ID is available.|12345abcde12345|||||||
|ecommerce.item_list_name|string|The human-readable name of the item list the item showed up in \(if sent with a view\_item\_list event\). If one is not available, populate with numerical index of which list this is on the page \(1-indexed\). For filter\_by\_group component, use that value.|filter\_by\_group, recommended\_products, recently\_viewed\_products|||||||
|ecommerce.items[n].item_brand|string|Item brand|Gucci|||||||
|ecommerce.items[n].item_category|string|Use this variable for the rateCode for the selected room|DBAR, CRP1S1|||||||
|ecommerce.items[n].item_category2|string|The Room Type Code|DK|||||||
|ecommerce.items[n].item_category3|string|Pipe separate value for Promo Code & Group Code, i.e. promoCode\|groupCode \(replace with actual values\)||||||||
|ecommerce.items[n].item_category4|integer|The number of adults included in the booking|2,3|||||||
|ecommerce.items[n].item_category5|integer|The number of children included in a booking|2, 3|||||||
|ecommerce.items[n].item_id|string|Item ID \(context-specific\).The product primary ID \(Hotel Code\)|PHXRST|||||||
|ecommerce.items[n].item_name|string|Full name of the hotel as listed on the website|Omni Scottsdale Resort & Spa at Montelucia|||||||
|ecommerce.items[n].item_variant|number|The \# of days in advance that the reservation is being made vs. the actual booking \(booking arrival date - reservation date\)|2, 20, 30|||||||

## Attached Notes

<p>This is event is for non hotel room product listing item clicked. e.g. <span style="font-weight: 400;">gift cards, spa appointments, golf tee times</span></p>
