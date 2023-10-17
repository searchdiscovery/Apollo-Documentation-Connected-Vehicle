# Form Started

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Form Started",
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

<p dir="auto">Fire whenever a user starts filling out a form.</p>
<p dir="auto">This event is generally fired after user input in the first form field. Historically this has been done via an HTMLElement change event on a form field, though it could be done via an HTMLElement focus event on a form field instead, if that proves easier to implement. It should only be fired once per unique form on page, but if that is too technically complicated to implement, it can be limited on the Adobe configuration side instead.</p>
