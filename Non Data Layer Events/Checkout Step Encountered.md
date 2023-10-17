# Checkout Step Encountered

### 

## Variable Definitions

| Attribute Name|Data Source Type|Data Source|Description|
| --- | --- | --- | --- |
|Checkout Step Encounters|Static|1|Description not provided|
|Set category to 'product'|Static|product|Description not provided|

## Attached Notes

<p><strong>The priceTier should be the product tier for SXM. </strong><em>(&lt; should be updated/reflected in GIT definitions...)</em></p>
<p>This event should be fired each time a user traverses between a subscription/enrollment flow step (ex. Account Register, Eligible Trial, Terms Accept, Payment, Review, Confirm, Package Selection etc...).</p>
<p>This event should not be 're-'fired if the user traverses back to the previous step. eg S1 &gt; S2 &gt; S3 &lt; S2 (do not fire event again on S2). <em>Adobe can be configured to ensure that a 'duplicated checkout step' does not occur, if the development work is overly complex.</em></p>