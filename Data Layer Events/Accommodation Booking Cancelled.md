# Accommodation Booking Cancelled

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ ecommerce: null });  // Clear the previous ecommerce object.
dataLayer.push({
  "event": "refund",
  "detailed_event": "Accommodation Booking Cancelled",
    "ecommerce": {
        "cancellation_id": "<cancellation_id>",
        "currency": "<currency>",
        "items": [
            {
                "item_id": "<item_id>",
                "item_name": "<item_name>",
                "price": <price>,
                "quantity": <quantity>
            }
        ],
        "reservation_id": "<reservation_id>",
        "transaction_id": "<transaction_id>",
        "value": <value>
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|ecommerce.cancellation_id|string|Captures the cancellation number associated with each booking cancellation.||||||||
|ecommerce.currency|string|The currency, in 3-letter ISO 4217 format.|USD, CAD|||||||
|ecommerce.items[n].item_id|string|Item ID \(context-specific\).The product primary ID \(Hotel Code\)|PHXRST|||||||
|ecommerce.items[n].item_name|string|Full name of the hotel as listed on the website|Omni Scottsdale Resort & Spa at Montelucia|||||||
|ecommerce.items[n].price|number|The monetary price of the item, in units of the specified currency parameter.|9.99|||||||
|ecommerce.items[n].quantity|integer|Item quantity.|1|||||||
|ecommerce.reservation_id|string|Captures the original reservation confirmation\/transaction ID associated with each booking.||^[a-zA-Z0-9]{6,20}$|6|20||||
|ecommerce.transaction_id|string|booking confirmation number \/ transaction id|40049476467|^[a-zA-Z0-9]{6,20}$|6|20||||
|ecommerce.value|number|The monetary value of the event.|7.77, 239.55, 659|||||||

## Attached Notes

<p>fires when a reservation has been cancelled and the cancellation confirmation info is displayed on the screen</p>
