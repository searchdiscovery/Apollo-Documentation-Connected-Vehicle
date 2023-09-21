# User Registered

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "User Registered",
    "user": {
        "custKey": "<custKey>",
        "hashedEmail": "<hashedEmail>",
        "loginStatus": "<loginStatus>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|user.custKey|string|Unique identifier of a customer.  Any id's considered PII must be hashed. ||||||||
|user.hashedEmail|string|The email address of a given user \(pre-hashed in the data layer with hashing algorithm of choice, such as MD5 or SHA-2\).|b642b4217b34b1e8d3bd915fc65c4452|||||||
|user.loginStatus|string|Describes the login state of the user|logged in, logged out, guest|||||||




