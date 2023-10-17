# Form Viewed

### This event is part of the page load sequence, including virtual page loads in the case of single page apps, and must be pushed between the `Page Load Started` and `Page Load Completed` events.

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Form Viewed",
    "form": {
        "formName": "<formName>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|form.formName|string|Plain text form name. Generally used if formID is not obtainable. |Payment Info, Mailing Address, Payment Address, Contact Us|||||||

## Attached Notes

<p>Fire whenever a user is presented with a form on a page. This could include a form scrolling into a user viewport (ie footer forms, below-the-fold forms), when a form is dynamically loaded, a 'pop-up' form, or when a page is contextually loaded for the purpose of completing a form.</p>
<p>This event should only be fired once per unique form on page; avoid scenarios where the user may scroll up/down page, and continously fire this event, when the form enters the user's viewport.</p>
