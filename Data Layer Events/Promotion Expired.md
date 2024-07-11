# Promotion Expired

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Promotion Expired",
    "page": {
        "pageName": "<pageName>",
        "vin_mask": "<vin_mask>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|page.pageName|string|Describes the page and its content specifically. |product - XYZ123, Mens - Tops - Sweaters, Order Confirmation|||||||
|page.vin_mask|string|Describes the customers Vehicle Identification Number \(VIN\). \*VIN should be hashed the same and as required. ex.  \*\*\*\*\*\*\*\*\*JT630290 \(3F4NKCAC8JT630290\)|\*\*\*\*\*\*\*\*\*JT630290 \(3F4NKCAC8JT630290\)|||||||




