# Navigation Link Clicked

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "click",
  "detailed_event": "Navigation Link Clicked",
    "event_data": {
        "component_ancestry": "<component_ancestry>",
        "identifier": "<identifier>",
        "link_url": "<link_url>",
        "region_ancestry": "<region_ancestry>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.component_ancestry|string|Captures the name or ID of the container within which navigation links are used.|Best Friends - Best Jeans, Puppy Love, Sail Away, Mens, Kids, Kids : Tops|||||||
|event_data.identifier|string|Captures the name or ID of the navigation links used.|All Hotels & Resorts,Offers|||||||
|event_data.link_url|string|Captures the site destination of the navigation links used.|https:\/\/www.example.com|||||||
|event_data.region_ancestry|string|Captures the name or ID of the region within which navigation links are used.|Top Nav, Footer Nav, Hero, Recommended, Also Shopped, Also Bought|||||||

## Attached Notes

<p>This should fire when a user clicks a navigation link, specifically a link or Button that takes the user to another location/page on the website (as opposed to a CTA button such as 'submit')</p>
