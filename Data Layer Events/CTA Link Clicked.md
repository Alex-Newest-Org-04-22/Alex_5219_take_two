# CTA Link Clicked

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "click",
  "detailed_event": "CTA Link Clicked",
    "event_data": {
        "category": "<category>",
        "component_ancestry": "<component_ancestry>",
        "identifier": "<identifier>",
        "region_ancestry": "<region_ancestry>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.category|string|Category or type of Call to Action \(CTA\) link.|External links \(view 3d tour,  book activities\)|||||||
|event_data.component_ancestry|string|Captures the name or ID of the container within which CTA links are used.||||||||
|event_data.identifier|string|Captures the ID associated with CTA links used.|act now, cancel, ok, 3456, 8765|||||||
|event_data.region_ancestry|string|Captures the name or ID of the region within which CTA links are used.|Top Nav, Footer Nav, Hero, Recommended, Also Shopped, Also Bought|||||||

## Attached Notes

<p>This should fire on links to external "conversions" in all instances where they can be found for hotel properties.&nbsp;</p>
<p>&nbsp;</p>
<p>This includes the following links (these are examples, code should be pushed to all instances):</p>
<ol class="p-rich_text_list p-rich_text_list__ordered" data-stringify-type="ordered-list" data-indent="0" data-border="0">
<li data-stringify-indent="0" data-stringify-border="0"><a class="c-link" tabindex="-1" href="https://www.omnihotels.com/hotels/homestead-virginia/golf" target="_blank" rel="noopener noreferrer" data-stringify-link="https://www.omnihotels.com/hotels/homestead-virginia/golf" data-sk="tooltip_parent" data-remove-tab-index="true">https://www.omnihotels.com/hotels/homestead-virginia/golf</a>&nbsp;- &ldquo;book tee time&rdquo;</li>
<li data-stringify-indent="0" data-stringify-border="0"><a class="c-link" tabindex="-1" href="https://www.omnihotels.com/media-center/multimedia" target="_blank" rel="noopener noreferrer" data-stringify-link="https://www.omnihotels.com/media-center/multimedia" data-sk="tooltip_parent" data-remove-tab-index="true">https://www.omnihotels.com/media-center/multimedia</a>&nbsp;- &ldquo;view digital library&rdquo;</li>
<li data-stringify-indent="0" data-stringify-border="0"><a class="c-link" tabindex="-1" href="https://www.omnihotels.com/hotels/homestead-virginia/spa" target="_blank" rel="noopener noreferrer" data-stringify-link="https://www.omnihotels.com/hotels/homestead-virginia/spa" data-sk="tooltip_parent" data-remove-tab-index="true">https://www.omnihotels.com/hotels/homestead-virginia/spa</a>&nbsp;- &ldquo;book your spa visit&rdquo;</li>
<li data-stringify-indent="0" data-stringify-border="0"><a href="https://www.omnihotels.com/hotels/dallas/meetings">https://www.omnihotels.com/hotels/dallas/meetings</a> - "view 3d tour"</li>
</ol>
