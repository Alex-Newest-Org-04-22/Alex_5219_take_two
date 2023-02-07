# Accommodation Booking Completed

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ ecommerce: null });  // Clear the previous ecommerce object.
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "purchase",
  "detailed_event": "Accommodation Booking Completed",
    "ecommerce": {
        "coupon": "<coupon>",
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
                "item_list_id": "<item_list_id>",
                "item_list_name": "<item_list_name>",
                "item_name": "<item_name>",
                "item_variant": <item_variant>,
                "location_id": "<location_id>",
                "price": <price>,
                "quantity": <quantity>
            }
        ],
        "payment_method": "<payment_method>",
        "reservation_id": "<reservation_id>",
        "tax": <tax>,
        "transaction_id": "<transaction_id>",
        "value": <value>
    },
    "event_data": {
        "addon_names": "<addon_names>",
        "addon_value": <addon_value>,
        "days_to_start_date": <days_to_start_date>,
        "end_date": "<end_date>",
        "local_taxes": <local_taxes>,
        "number_of_adults": <number_of_adults>,
        "number_of_children": <number_of_children>,
        "people": <people>,
        "resort_fee": <resort_fee>,
        "start_date": "<start_date>",
        "subtotal": <subtotal>,
        "total_nights": <total_nights>,
        "total_rooms": <total_rooms>
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|ecommerce.coupon|string|Order-level coupon code used for a purchase.|summer\_fun|||||||
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
|ecommerce.items[n].item_list_id|string|The computer-readable machine name of the list the item showed up in \(if sent with a view\_item\_list event\). Use UUID provided by the component if no more specific ID is available.|12345abcde12345|||||||
|ecommerce.items[n].item_list_name|string|The human-readable name of the item list the item showed up in \(if sent with a view\_item\_list event\). If one is not available, populate with numerical index of which list this is on the page \(1-indexed\). For filter\_by\_group component, use that value.|filter\_by\_group, recommended\_products, recently\_viewed\_products|||||||
|ecommerce.items[n].item_name|string|Full name of the hotel as listed on the website|Omni Scottsdale Resort & Spa at Montelucia|||||||
|ecommerce.items[n].item_variant|number|The \# of days in advance that the reservation is being made vs. the actual booking \(booking arrival date - reservation date\)|2, 20, 30|||||||
|ecommerce.items[n].location_id|string|The location associated with the event. If possible, set to the Google Place ID that corresponds to the associated item. Can also be overridden to a custom location ID string.|L\_12345|||||||
|ecommerce.items[n].price|number|The monetary price of the item, in units of the specified currency parameter.|9.99|||||||
|ecommerce.items[n].quantity|integer|Item quantity.|1|||||||
|ecommerce.payment_method|string|Captures the payment methods used for a transaction \(i.e. credit card, Visa, MasterCard, Amex, Paypal, purchase order, etc\).|Credit Card, PayPal, Mastercard, Visa, Amex, Discover|||||||
|ecommerce.reservation_id|string|Captures the original reservation confirmation\/transaction ID associated with each booking.||^[a-zA-Z0-9]{6,20}$|6|20||||
|ecommerce.tax|number|Tax cost associated with a transaction.|1.11|||||||
|ecommerce.transaction_id|string|booking confirmation number \/ transaction id|40049476467|^[a-zA-Z0-9]{6,20}$|6|20||||
|ecommerce.value|number|The monetary value of the event.|7.77, 239.55, 659|||||||
|event_data.addon_names|string|Pipe delimited list of Add-On names included in completed hotel booking|LATE CHECK OUT 2PM\|$200 RESORT CREDIT FOR $180|||||||
|event_data.addon_value|number|Total sum value of add-ons included in a completed hotel room booking|280.00|||||||
|event_data.days_to_start_date|integer|Captures the number of days prior to booking's check-in date|1, 2, 3, 4, 5|||||||
|event_data.end_date|string|Captures the end date in a booking.|2022-10-28, 2023-01-15|^([0-9]{4})-(1[0-2]|0[1-9])-(3[01]|0[1-9]|[12][0-9])$||||||
|event_data.local_taxes|number|Local taxes, itemized separately from primary tax metric||||||||
|event_data.number_of_adults|integer|Captures the number of adults entered in search criteria.|1, 2, 3, 4, 5||||1|||
|event_data.number_of_children|integer|Captures the number of children entered in search criteria.|1, 2, 3, 4, 5|||||||
|event_data.people|number|Captures the number of people entered in search criteria.|1, 2, 3, 4, 5||||1|||
|event_data.resort_fee|number|DL metric for hotel booking resort fee||||||||
|event_data.start_date|string|Captures the start date in a booking|2022-10-22, 2023-01-15|^([0-9]{4})-(1[0-2]|0[1-9])-(3[01]|0[1-9]|[12][0-9])$||||||
|event_data.subtotal|number|DL metric for hotel booking Subtotal||||||||
|event_data.total_nights|integer|captures the total number of nights in a booking including all rooms||||||||
|event_data.total_rooms|integer|captures the total number of rooms in a booking||||||||

## Attached Notes

<p>When the user has completed booking a room on the order confirmation page.</p>
<p>&nbsp;</p>
<p>include price breakout:</p>
<ul>
<li>price = base room rate</li>
<li>value = room rate * nights for the room in this item location</li>
<li>Resort Fee</li>
<li>Taxes</li>
<li>Local Taxes</li>
<li>Addons</li>
<li>Sub Total</li>
<li>Total Price</li>
</ul>
