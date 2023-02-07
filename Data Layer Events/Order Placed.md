# Order Placed

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ ecommerce: null });  // Clear the previous ecommerce object.
dataLayer.push({
  "event": "purchase",
  "detailed_event": "Order Placed",
    "ecommerce": {
        "currency": "<currency>",
        "items": [
            {
                "coupon": "<coupon>",
                "discount": <discount>,
                "item_brand": "<item_brand>",
                "item_category": "<item_category>",
                "item_category2": "<item_category2>",
                "item_category3": "<item_category3>",
                "item_category4": <item_category4>,
                "item_category5": <item_category5>,
                "item_id": "<item_id>",
                "item_name": "<item_name>",
                "item_variant": <item_variant>,
                "price": <price>,
                "quantity": <quantity>
            }
        ],
        "ship_to_postal_code": "<ship_to_postal_code>",
        "ship_to_state_or_province": "<ship_to_state_or_province>",
        "transaction_id": "<transaction_id>",
        "value": <value>
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|ecommerce.currency|string|The currency, in 3-letter ISO 4217 format.|USD, CAD|||||||
|ecommerce.items[n].coupon|string|Item-level coupon code used for a purchase.|SUMMER\_FUN|||||||
|ecommerce.items[n].discount|number|Monetary value of discount associated with a purchase.|2.22|||||||
|ecommerce.items[n].item_brand|string|Item brand|Gucci|||||||
|ecommerce.items[n].item_category|string|Use this variable for the rateCode for the selected room|DBAR, CRP1S1|||||||
|ecommerce.items[n].item_category2|string|The Room Type Code|DK|||||||
|ecommerce.items[n].item_category3|string|Pipe separate value for Promo Code & Group Code, i.e. promoCode\|groupCode \(replace with actual values\)||||||||
|ecommerce.items[n].item_category4|integer|The number of adults included in the booking|2,3|||||||
|ecommerce.items[n].item_category5|integer|The number of children included in a booking|2, 3|||||||
|ecommerce.items[n].item_id|string|Item ID \(context-specific\).The product primary ID \(Hotel Code\)|PHXRST|||||||
|ecommerce.items[n].item_name|string|Full name of the hotel as listed on the website|Omni Scottsdale Resort & Spa at Montelucia|||||||
|ecommerce.items[n].item_variant|number|The \# of days in advance that the reservation is being made vs. the actual booking \(booking arrival date - reservation date\)|2, 20, 30|||||||
|ecommerce.items[n].price|number|The monetary price of the item, in units of the specified currency parameter.|9.99|||||||
|ecommerce.items[n].quantity|integer|Item quantity.|1|||||||
|ecommerce.ship_to_postal_code|string|Captures the postal code for shipping.|53533, 30381, M1R 0E9, M3C 0C1|||||||
|ecommerce.ship_to_state_or_province|string|Captures the state or province associated with the shipping address|WI, GA, NB, ON|||||||
|ecommerce.transaction_id|string|booking confirmation number \/ transaction id|40049476467|^[a-zA-Z0-9]{6,20}$|6|20||||
|ecommerce.value|number|The monetary value of the event.|7.77, 239.55, 659|||||||

## Attached Notes

<p>This is event is for non hotel room purchases. gift cards, etc</p>
