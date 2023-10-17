# Form Submission Failed

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Form Submission Failed",
    "form": {
        "formError": "<formError>",
        "formName": "<formName>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|form.formError|string|Error text or code describing a form error.  This is the form-level error.|Credit card declined, Required entries missing, EC3456, EC8976|||||||
|form.formName|string|Plain text form name. Generally used if formID is not obtainable. |Payment Info, Mailing Address, Payment Address, Contact Us|||||||

## Attached Notes

<p dir="auto">Fire whenever a user unsuccessfully completes a form submission.</p>
<p dir="auto">This is in contrast to&nbsp;<code>form_complete</code> (Form Submission Succeeded) which occurs when a submission succeeds. This event should be utilized to capture form post submission errors, not form field error/validation messaging.</p>
