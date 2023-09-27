# Page Load Started

### Page Load Started is part of the page load sequence, including virtual page loads in the case of single page apps, and must be the first event pushed in the page load event sequence.

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Page Load Started",
    "page": {
        "action_taken": "<action_taken>",
        "adobe_user_id": "<adobe_user_id>",
        "customer_flow": "<customer_flow>",
        "oem": "<oem>",
        "pageCategory": "<pageCategory>",
        "pageExperience": "<pageExperience>",
        "pageName": "<pageName>",
        "pageType": "<pageType>",
        "siteCountry": "<siteCountry>",
        "siteExperience": "<siteExperience>",
        "siteLanguage": "<siteLanguage>",
        "siteName": "<siteName>",
        "subsection": "<subsection>",
        "subsection2": "<subsection2>",
        "subsection3": "<subsection3>",
        "vin_mask": "<vin_mask>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|page.action_taken|string|Datasource path for Action Taken attribute.||||||||
|page.adobe_user_id|string|Tracks the assigned Adobe User ID||||||||
|page.customer_flow|string|Datasource for Customer Flow.||||||||
|page.oem|string|OEM Datasource|GM12345678|[A-Za-z0-9]+||||||
|page.pageCategory|string|General category or Site Section of the page. Top level of page hierarchy.|Home, About Us, Shop, Account, Blog, Investors|||||||
|page.pageExperience|string|When a feature ramp up is taking place, capture a code to identify users receiving that feature's experience.||||||||
|page.pageName|string|Describes the page and its content specifically. |product - XYZ123, Mens - Tops - Sweaters, Order Confirmation|||||||
|page.pageType|string|Describes what purpose the page serves. Often aligns with the CMS template.|Home, Event Detail, Property Detail, Product Listing, Blog Post, Shopping Cart|||||||
|page.siteCountry|string|Indicates the primary country served by the site. ISO 3166 \(alpha-2\) Uppercase.|US, CA, FR, UK|^[A-Z]{2}$||||||
|page.siteExperience|string|Describes the version of the site that is being shown|Responsive, Mobile, Desktop|||||||
|page.siteLanguage|string|Language in which the site is presented ISO 639-1 code. |en-us, en-gb, ch-cn, fr-ca, fr-fr, da|^[a-z]{2}([-]{1}[a-z]{2}){0,1}$||||||
|page.siteName|string|Common language used within the business to refer to the website. May be specific County Sites.|Prospecting-EU, Prospecting-US, Member Portal, Shop-CA, Shop-US, Shop-EU|||||||
|page.subsection|string|First sub-level of hierarchy under pageCategory or Site Section. |Shop &gt; Kids, Shop &gt; Mens, Shop &gt; Womens|||||||
|page.subsection2|string|Second sub-level of hierarchy under pageCategory or Site Section. |Shop &gt; Kids &gt; Tops, Shop &gt; Mens &gt; Shoes|||||||
|page.subsection3|string|Third sub-level of hierarchy under pageCategory or Site Section. |Shop &gt; Kids &gt; Tops &gt; Tees, Shop &gt; Mens &gt; Shoes &gt; Oxfords|||||||
|page.vin_mask|string|Datasource for the variable\/value for a users VIN.||||||||




