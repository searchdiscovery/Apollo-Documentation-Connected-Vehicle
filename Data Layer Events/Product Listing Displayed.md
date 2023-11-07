# Product Listing Displayed

### This event is part of the page load sequence, including virtual page loads in the case of single page apps, and must be pushed between the `Page Load Started` and `Page Load Completed` events.

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Product Listing Displayed",
    "listingDisplayed": {
        "listing": [
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
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|listingDisplayed.listing[n].price.priceTier|string|Describes the general pricing tier of a product. \(Good, Better, Best\)|Good, Better, Best, Bronze, Silver, Gold|||||||
|listingDisplayed.listing[n].productInfo.name|string|Name of the product or offering.  Should be unique and 1:1 with productID|Oceana, Corsica, Flame Tech, Air Jordan 88|||||||
|listingDisplayed.listing[n].productInfo.package_id|string|Describes the Package ID|12345abce|||||||
|listingDisplayed.listing[n].productInfo.productDiscount|string|Describes the Product Discount \(order\).|50% Off, Free Trial|||||||
|listingDisplayed.listing[n].productInfo.productID|string|Unique Identifier of a product or offering.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level above SKU for products with SKU variants. |155, 65588, 987764448|||||||
|listingDisplayed.listing[n].productInfo.variant_id|string|Descriptions the Variant ID within a listing of products.|123456789, variant 1, My Varient|||||||




