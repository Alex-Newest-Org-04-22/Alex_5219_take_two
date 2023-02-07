# Form Started

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "form_start",
  "detailed_event": "Form Started",
    "event_data": {
        "identifier": "<identifier>",
        "name": "<name>",
        "type": "<type>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.identifier|string|Captures the unique ID of the form.|F-0113, 2543, CU001, PI-0988|||||||
|event_data.name|string|Captures the human-friendly name of the form.|Payment Info, Mailing Address, Payment Address, Contact Us|||||||
|event_data.type|string|Captures the sub-type of form:
for the Contact Us form: Hotel Feedback, General Inquiries, etc.
for the Request for Proposal form: Meeting Wedding Social|Hotel Feedback, General Inquiries, Meeting, Wedding, Social|||||||

## Attached Notes

<p>This will fire when a user begins to enter inputs into a form, e.g. the Meetings and Events RFP form, located at https://www.omnihotels.com/meetings/rfp</p>
