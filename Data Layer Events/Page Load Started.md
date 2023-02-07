# Page Load Started

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ page_data: null });  // Clear the previous page_data object.
dataLayer.push({
  "event": "page_load_started",
  "detailed_event": "Page Load Started",
    "page_data": {
        "country": "<country>",
        "language": "<language>",
        "name": "<name>",
        "page_location": "<page_location>",
        "page_path": "<page_path>",
        "page_title": "<page_title>",
        "platform_version": "<platform_version>",
        "site_section": "<site_section>",
        "weekday_or_weekend": "<weekday_or_weekend>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|page_data.country|string|The country associated with the current page.|US, CA, FR, UK|||||||
|page_data.language|string|The language of the current page, usually pulled from the &lt;html&gt; tag lang attribute.|en-us, en-gb, ch-cn, fr-ca, fr-fr|||||||
|page_data.name|string|Captures the name of the page the user is on||||||||
|page_data.page_location|string|The url of the page currently being viewed.||||||||
|page_data.page_path|string|Captures the path portion of the page URL.||||||||
|page_data.page_title|string|The title of the page currently being viewed, generally available in &lt;title&gt;.|Omni Scottsdale Resort & Spa at Montelucia \| Scottsdale, AZ Resorts, Omni Hotels & Resorts \| Book Your Stay|||||||
|page_data.platform_version|string|The platform used to share content.|Sitecore XP 8.2, Booking Engine|||||||
|page_data.site_section|string|The section of the site that the current page resides in. brand or hotel for front end, booking engine for all booking engine pages|brand, hotel, booking engine|||||||
|page_data.weekday_or_weekend|string|Whether it was a weekday or weekend when the activity occurred.||||||||

## Attached Notes

<p>This is information about the page.&nbsp; We will want to fire the events in this sequence.<br />Page Load Started &gt; User Detected &gt; Page Load Completed<br /><br />For the Booking Engine we will want to replace page_location with the virtual page url.</p>
<ul>
<li style="font-weight: 400;" aria-level="2"><span style="font-weight: 400;">Step 2: <strong>Select Room page</strong> (page_location: https://booking.omnihotels.com/booking-engine/select-room)</span></li>
<li style="font-weight: 400;" aria-level="2"><span style="font-weight: 400;">Step 3: <strong>Custom Add Ons/Dynamic Package</strong> (page_location: https://booking.omnihotels.com/booking-engine/enhance-stay)</span></li>
<li style="font-weight: 400;" aria-level="2"><span style="font-weight: 400;">Step 4: <strong>Guest information and Payment</strong> (page_location: https://booking.omnihotels.com/booking-engine/guest-information)</span></li>
<li style="font-weight: 400;" aria-level="2"><span style="font-weight: 400;">Step 5: <strong>Confirmation</strong> (page_location: https://booking.omnihotels.com/booking-engine/booking-confirmation)</span></li>
<li style="font-weight: 400;" aria-level="2"><span style="font-weight: 400;">There are a few places where a user can go off course from this path. If they select flexible dates or if there is not availability they will be directed to an interim page between step 1 and 2. Or they ca select it from step 2.)</span></li>
<ul>
<li style="font-weight: 400;" aria-level="3"><span style="font-weight: 400;">page_location: https://booking.omnihotels.com/booking-engine/check-availability-calendar</span></li>
</ul>
<li style="font-weight: 400;" aria-level="2"><span style="font-weight: 400;">After Confirmation a user can do a few things that we will want to measure as well.</span></li>
<ul>
<li style="font-weight: 400;" aria-level="3"><span style="font-weight: 400;">They can add a room upgrade request</span></li>
<li style="font-weight: 400;" aria-level="3"><span style="font-weight: 400;"><strong>Request</strong> &ndash; page_location: https://booking.omnihotels.com/booking-engine/upgrade-request</span></li>
<li style="font-weight: 400;" aria-level="3"><span style="font-weight: 400;"><strong>Upgrade Confirmation</strong> &ndash; page_location: https://booking.omnihotels.com/booking-engine/upgrade-confirmation</span></li>
</ul>
</ul>
