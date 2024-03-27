# Cancellation Custom Click

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Cancellation Custom Click",
    "click": {
        "Text": "<Text>"
    },
    "page": {
        "pageName": "<pageName>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|click.Text|string|Captures the clicked text|Enroll Now, Get This Deal, Activate Trial|||||||
|page.pageName|string|Describes the page and its content specifically. |product - XYZ123, Mens - Tops - Sweaters, Order Confirmation|||||||

## Attached Notes

<p>The event should be fired each time a user clicks on a button or a clickable link in the cancellation flow, including:</p>
<ol>
<li>"Keep Subscription" button</li>
<li>"Continue Cancellation" button</li>
<li>"Cancel Subscription" button</li>
<li>All clickable links in the cancellation flow, includes:<br />- packagename.com&nbsp;<br />- See Complete List<br />- See All Offers<br />- Package Details<br />- Offer Details<br />- Profile</li>
</ol>
<p>The event can be fired for clicks on "Get This Deal", "Activate Trial" and "Enroll Now" if it makes it easier on the dev side. We have these three buttons tracked in another event.</p>
