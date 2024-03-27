# Enrollment_CancellationFlow

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Enrollment_CancellationFlow",
    "click": {
        "Text": "<Text>"
    },
    "page": {
        "pageName": "<pageName>",
        "vin_mask": "<vin_mask>"
    },
    "product": [
        {
            "productInfo": {
                "name": "<name>",
                "package_id": "<package_id>"
            }
        }
    ]
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|click.Text|string|Captures the clicked text|Enroll Now, Get This Deal, Activate Trial|||||||
|page.pageName|string|Describes the page and its content specifically. |product - XYZ123, Mens - Tops - Sweaters, Order Confirmation|||||||
|page.vin_mask|string|Describes the customers Vehicle Identification Number \(VIN\). \*VIN should be hashed the same and as required. ex.  \*\*\*\*\*\*\*\*\*JT630290 \(3F4NKCAC8JT630290\)|\*\*\*\*\*\*\*\*\*JT630290 \(3F4NKCAC8JT630290\)|||||||
|product[n].productInfo.package_id|string|The selected subscription Package ID. eg the ID associated with Package  $100\/year|123456789|||||||

## Attached Notes

<p>This event should be fired each time a user enrolls in a package or activates a trial offered during the cancellation flow. Specifically:</p>
<ul>
<li>Click on "Enroll Now" (nextPricePackage screen)</li>
<li>Click on "Get This Deal" (nextBestOffer screen)</li>
<li>Click on "Activate Trial" (nextBestOffer screen)</li>
</ul>
