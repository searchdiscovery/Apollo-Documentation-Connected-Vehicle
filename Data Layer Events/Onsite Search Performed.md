# Onsite Search Performed

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Onsite Search Performed",
    "onsiteSearch": {
        "keyword": {
            "searchTerm": "<searchTerm>"
        }
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|onsiteSearch.keyword.searchTerm|string|Describes the search keyword used after auto-correct, auto-complete, or keyword suggestion. |bluth, blue, red lobster|||||||

## Attached Notes

<p>Fire this event whenever a user performs a search of any kind. This includes product searches, content searches, resource searches, etc... this event does not require a Onsite Search Succeeded event to be fired subsequently.</p>
