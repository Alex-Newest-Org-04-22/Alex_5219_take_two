# Onsite Search Performed

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "search",
  "detailed_event": "Onsite Search Performed",
    "event_data": {
        "days_to_start_date": <days_to_start_date>,
        "end_date": "<end_date>",
        "number_of_adults": <number_of_adults>,
        "number_of_children": <number_of_children>,
        "onsite_search_date_count": <onsite_search_date_count>,
        "people": <people>,
        "search_term": "<search_term>",
        "start_date": "<start_date>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.days_to_start_date|integer|Captures the number of days prior to booking's check-in date|1, 2, 3, 4, 5|||||||
|event_data.end_date|string|Captures the end date in a booking.|2022-10-28, 2023-01-15|^([0-9]{4})-(1[0-2]|0[1-9])-(3[01]|0[1-9]|[12][0-9])$||||||
|event_data.number_of_adults|integer|Captures the number of adults entered in search criteria.|1, 2, 3, 4, 5||||1|||
|event_data.number_of_children|integer|Captures the number of children entered in search criteria.|1, 2, 3, 4, 5|||||||
|event_data.onsite_search_date_count|integer|Captures the number of dates requested in search criteria.|8, 1, 5, 6, 7, 10||||1|||
|event_data.people|number|Captures the number of people entered in search criteria.|1, 2, 3, 4, 5||||1|||
|event_data.search_term|string|Captures the search text used in on-site searches.|scottsdale, california, beach|||||||
|event_data.start_date|string|Captures the start date in a booking|2022-10-22, 2023-01-15|^([0-9]{4})-(1[0-2]|0[1-9])-(3[01]|0[1-9]|[12][0-9])$||||||

## Attached Notes

<p>registers the event and captures inputs from initial search widget (on homepage and elsewhere).</p>
<p>&nbsp;</p>
<p>Also fires when a user modifies a search, also from the search widget, to change dates, # of guests, etc.</p>
