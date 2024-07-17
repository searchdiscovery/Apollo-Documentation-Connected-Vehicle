# Promotion Discounts

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Promotion Discounts",
    "page": {
        "vin_mask": "<vin_mask>"
    },
    "product": [
        {
            "productInfo": {
                "name": "<name>",
                "productDiscount": "<productDiscount>"
            }
        }
    ],
    "transaction": {
        "item": [
            {
                "productInfo": {
                    "priceTier": "<priceTier>"
                }
            }
        ]
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|page.vin_mask|string|Describes the customers Vehicle Identification Number \(VIN\). \*VIN should be hashed the same and as required. ex.  \*\*\*\*\*\*\*\*\*JT630290 \(3F4NKCAC8JT630290\)|\*\*\*\*\*\*\*\*\*JT630290 \(3F4NKCAC8JT630290\)|||||||
|product[n].productInfo.name|string|The name of the selected subscription package. eg 'Package 1234'|Package 1234|||||||
|product[n].productInfo.productDiscount|string|Describes Product Discount attribute for the subscription package.|50% Off, Free Trial|||||||
|transaction.item[n].productInfo.priceTier|string|Describes the subscription pricing tier of a selected subscription package. \(eg 3-month Trial, 6-Month Trial, $100mo, etc..\)|3-month Trial, 6-Month Trial, $100mo|||||||




