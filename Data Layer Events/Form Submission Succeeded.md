# Form Submission Succeeded

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Form Submission Succeeded",
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

<p dir="auto">Fire whenever a user successfully completes a form submission.</p>
<p dir="auto">This event is fired when form post input is successfully received and processed by the server. This is in contrast to (Form Submission Failed) which occurs when a form submission is attempted but an error occurs and the form post input is not recieved and/or processed successfully.</p>
