# Checkout Step Encountered

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Checkout Step Encountered",
    "eventDetails": {
        "checkoutStep": "<checkoutStep>"
    },
    "product": [
        {
            "price": {
                "priceTier": "<priceTier>"
            },
            "productInfo": {
                "name": "<name>",
                "package_id": "<package_id>",
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
|eventDetails.checkoutStep|string|Describes a discrete step in the checkout flow.|Account Registration, Free Term Information, T\/C Acceptance, Payment, Review|||||||
|product[n].price.priceTier|string|Describes the subscription pricing tier of a selected subscription package. \(eg 3-month Trial, 6-Month Trial, $100mo, etc..\)|3-month, 6-month, $100-month, $400-year|||||||
|product[n].productInfo.name|string|The name of the selected subscription package. eg 'Package 1234'|Package 1234|||||||
|product[n].productInfo.package_id|string|The selected subscription Package ID. eg the ID associated with Package  $100\/year|123456789|||||||
|product[n].productInfo.productID|string|Unique Identifier of a product or offering.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level above SKU for products with SKU variants. |155, 65588, 987764448|||||||
|product[n].productInfo.variant_id|string|The selected subscription package \(add-on\) Variant ID. eg the ID associated with any subscription package \(add-on\) variant, if applicable.|123456789|||||||

## Attached Notes

<p><strong>The priceTier should be the product tier for SXM. </strong></p>
<p>This event should be fired each time a user traverses between a subscription/enrollment flow step (ex. Account Register, Eligible Trial, Terms Accept, Payment, Review, Confirm, Package Selection etc...).</p>
<p>This event should not be 're-'fired if the user traverses back to the previous step. eg S1 &gt; S2 &gt; S3 &lt; S2 (do not fire event again on S2). <em>Adobe can be configured to ensure that a 'duplicated checkout step' does not occur, if the development work is overly complex.</em></p>
