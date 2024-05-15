# Error

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Error",
    "error": {
        "errorCode": "<errorCode>",
        "errorMessage": "<errorMessage>"
    },
    "form": {
        "formField": "<formField>",
        "formName": "<formName>"
    },
    "page": {
        "pageName": "<pageName>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|error.errorCode|string|Error code or Error message presented to the user|Credit Card Authorization Failed , EC345, Form is incomplete|||||||
|error.errorMessage|string|The error message displayed to the users||||||||
|form.formField|string|Captures the field name|Last Name, Address, Zip Code, CC|||||||
|form.formName|string|Plain text form name. Generally used if formID is not obtainable. |Payment Info, Mailing Address, Payment Address, Contact Us|||||||
|page.pageName|string|Describes the page and its content specifically. |product - XYZ123, Mens - Tops - Sweaters, Order Confirmation|||||||




