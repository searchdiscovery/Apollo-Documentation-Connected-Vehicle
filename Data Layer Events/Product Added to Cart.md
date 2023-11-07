# Product Added to Cart

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Product Added to Cart",
    "product": [
        {
            "price": {
                "priceTier": "<priceTier>"
            },
            "productInfo": {
                "name": "<name>",
                "package_id": "<package_id>",
                "productDiscount": "<productDiscount>",
                "productID": "<productID>",
                "variant_id": "<variant_id>"
            }
        }
    ]
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|product[n].price.priceTier|string|Describes the subscription pricing tier of a selected subscription package. \(eg 3-month Trial, 6-Month Trial, $100mo, etc..\)|3-month, 6-month, $100-month, $400-year|||||||
|product[n].productInfo.package_id|string|The selected subscription Package ID. eg the ID associated with Package  $100\/year|123456789|||||||
|product[n].productInfo.productDiscount|string|Describes Product Discount attribute for the subscription package.|50% Off, Free Trial|||||||
|product[n].productInfo.productID|string|Unique Identifier of a product or offering.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level above SKU for products with SKU variants. |155, 65588, 987764448|||||||
|product[n].productInfo.variant_id|string|The selected subscription package \(add-on\) Variant ID. eg the ID associated with any subscription package \(add-on\) variant, if applicable.|123456789|||||||




