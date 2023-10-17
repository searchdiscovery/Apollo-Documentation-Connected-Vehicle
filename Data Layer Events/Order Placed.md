# Order Placed

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Order Placed",
    "transaction": {
        "item": [
            {
                "price": {
                    "sellingPrice": "<sellingPrice>"
                },
                "productInfo": {
                    "name": "<name>",
                    "package_id": "<package_id>",
                    "priceTier": "<priceTier>",
                    "productID": "<productID>",
                    "variant_id": "<variant_id>"
                },
                "quantity": <quantity>,
                "tax": "<tax>",
                "voucherDiscount": {
                    "orderLevelDiscountAmount": "<orderLevelDiscountAmount>",
                    "orderLevelDiscountCode": "<orderLevelDiscountCode>"
                }
            }
        ],
        "payment": [
            {
                "paymentGateway": "<paymentGateway>",
                "paymentID": "<paymentID>"
            }
        ],
        "purchaseID": "<purchaseID>",
        "total": {
            "currency": "<currency>"
        }
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|transaction.item[n].price.sellingPrice|string|String representation of the price paid after coupons or discounts. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||
|transaction.item[n].productInfo.name|string|Product 'Name' utilized in the order transaction, item-level.||||||||
|transaction.item[n].productInfo.package_id|string|The selected subscription Package ID. eg the ID associated with Package  $100\/year \*\(item-level\)|123456789|||||||
|transaction.item[n].productInfo.priceTier|string|Describes the subscription pricing tier of a selected subscription package. \(eg 3-month Trial, 6-Month Trial, $100mo, etc..\)|3-month Trial, 6-Month Trial, $100mo|||||||
|transaction.item[n].productInfo.productID|string|Unique Identifier of a product or offering.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level above SKU for products with SKU variants. |155, 65588, 987764448|||||||
|transaction.item[n].productInfo.variant_id|string|The selected subscription package \(add-on\) Variant ID. eg the ID associated with any subscription package \(add-on\) variant, if applicable. \*\(item-level\)|123456789|||||||
|transaction.item[n].quantity|integer|Integer number of products being acted upon \(added to a cart, removed from wishlist, purchased, reserved\)|1, 2, 3, 4, 5||||1|||
|transaction.item[n].tax|string|String representation of the tax collected at a shipment level for a transaction. Positive. Up to two decimal places for cents. No currency symbol.|5.05, 20, 10.22, 9.2|^[0-9]*(\.[0-9]{1,2})?$||||||
|transaction.item[n].voucherDiscount.orderLevelDiscountAmount|string|String representation of an order level discount applied to an item in a transaction. Positive. Up to two decimal places for cents. No currency symbol.|5, 20, 10.22, 19.2|^[0-9]*(\.[0-9]{1,2})?$||||||
|transaction.item[n].voucherDiscount.orderLevelDiscountCode|string|Order Level Discount code applied at the item level of a transaction. |FRIENDSANDFAMILY20, EASTER10|||||||
|transaction.payment[n].paymentGateway|string|Captures the digital payment gateway was used to complete transactions for orders?|PayPal, Stripe|||||||
|transaction.payment[n].paymentID|string|Unique identifier of a payment.  Typically an integration key from a back-end system.|ZPH-87698-098|||||||
|transaction.purchaseID|string|Unique identifier of the purchase. Max Length 20. Used as Unique ID of the purchase or deduplication.|ABC-132456789, DEF-132456789, 0987654567|^[a-zA-Z0-9]{6,20}$|6|20||||
|transaction.total.currency|string|Currency of the transaction. ISO 4217 \(3 character alpha\), uppercase |USD, CAD, GBP, CHF|^[A-Z]{3}$|3|3||||

## Attached Notes

<p>Fire this event when the user successfully completes the order/purchase (successful form post) of a enrollment/subscription.</p>
