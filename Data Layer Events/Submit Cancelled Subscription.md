# Submit Cancelled Subscription

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Submit Cancelled Subscription",
    "itemSelected": "<itemSelected>",
    "product": [
        {
            "productInfo": {
                "name": "<name>",
                "package_id": "<package_id>",
                "subs_label": "<subs_label>"
            }
        }
    ]
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|itemSelected|string|Captures the count of selected and unselected items|2\|3|||||||
|product[n].productInfo.package_id|string|The selected subscription Package ID. eg the ID associated with Package  $100\/year|123456789|||||||
|product[n].productInfo.subs_label|string|The existing subscription label of the selected package|trial|||||||

## Attached Notes

<p>This event should be fired each time a user hits "Continue Cancellation" on the selectPackage screen in the cancellation flow</p>
