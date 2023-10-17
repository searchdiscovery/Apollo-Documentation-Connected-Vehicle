# User Registration Errored

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "User Registration Errored",
    "user": {
        "registrationError": "<registrationError>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|user.registrationError|string|Captures the registration error code or message associated with user registrations.|Form is incomplete, EC345, Invalid field entry|||||||

## Attached Notes

<p dir="auto">Fire whenever a user unsuccessfully completes a 'registration' form submission.</p>
<p dir="auto">This is in contrast to (User Registered) which occurs when a 'registration' submission succeeds. This event should be utilized to capture form post submission errors, not form field error/validation messaging.</p>
