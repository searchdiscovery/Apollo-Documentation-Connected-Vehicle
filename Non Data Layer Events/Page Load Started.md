# Page Load Started

### 

## Variable Definitions

| Attribute Name|Data Source Type|Data Source|Description|
| --- | --- | --- | --- |
|Adobe User ID|Custom Code|marketingCloudVisitorID;|Describes the assigned Adobe User ID. \(MCID\)|
|Campaign Tracking (s.campaign)|Query String|cid|Description not provided|
|Host Name (s.server)|Custom Code|hostname;|Description not provided|
|IP Address (evar)|Custom Code|//via AA Launch|Describes the IP Address of the current user.|
|Launch Build Info|Custom Code|name;
}
return  buildDate  + "|" + enviroment + "|" + property;|Datasource for Launch Build info.|
|URL (Full)|Custom Code|href;|Description not provided|
|URL Path|Custom Code|pathname;|Description not provided|
|URL Query String|Custom Code|search;|Description not provided|
|UTM Campaign|Query String|utm_campaign|Describes the UTM Campaign parameter provided for by URI query string parameter.|
|UTM Medium|Query String|utm_medium|Describes the UTM Medium parameter provided for by URI query string parameter.|
|UTM Source|Query String|utm_source|Describes the UTM Source parameter provided for by URI query string parameter.|

## Attached Notes

<p class="p1"><span class="s1">Page Load Started is part of the page load sequence, including virtual page loads in the case of single page apps, and must be the <strong>first event pushed</strong> in the page load event sequence.</span></p>