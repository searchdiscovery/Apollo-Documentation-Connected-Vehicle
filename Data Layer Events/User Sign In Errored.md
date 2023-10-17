# User Sign In Errored

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "User Sign In Errored",
    "user": {
        "loginStatus": "<loginStatus>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|user.loginStatus|string|Describes the login state of the user|logged in, logged out, guest|||||||

## Attached Notes

<p dir="auto">Fire whenever a user unsuccessfully completes a 'user sign in' form submission.</p>
<p dir="auto">This is in contrast to (User Signed In) which occurs when a 'user sign in' submission succeeds. This event should be utilized to capture form post submission errors, not form field error/validation messaging.</p>
