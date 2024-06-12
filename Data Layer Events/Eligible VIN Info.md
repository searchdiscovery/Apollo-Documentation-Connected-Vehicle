# Eligible VIN Info

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Eligible VIN Info",
    "page": {
        "vin_mask": "<vin_mask>"
    },
    "service": {
        "serviceName": "<serviceName>"
    },
    "veh": {
        "vehInfo": "<vehInfo>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|page.vin_mask|string|Describes the customers Vehicle Identification Number \(VIN\). \*VIN should be hashed the same and as required. ex.  \*\*\*\*\*\*\*\*\*JT630290 \(3F4NKCAC8JT630290\)|\*\*\*\*\*\*\*\*\*JT630290 \(3F4NKCAC8JT630290\)|||||||
|service.serviceName|string|Populate all listed eligible services for a VIN. Use "\|" as the delimiter between services|Maintenance Alert\|Remote Battery Status|||||||
|veh.vehInfo|string|Populate the vehicle details with this format: Make\|Model\|Year|Nissan\|Sentra\|2022|||||||




