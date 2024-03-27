# cancelSubscription

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "cancelSubscription",
    "cancelReason": "<cancelReason>"
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|cancelReason|string|Tracking reason for cancelling||||||||

## Attached Notes

<p>This event should be fired each time a user hits "Cancel Subscription" on the reviewCancellation screen</p>
