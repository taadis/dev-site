---
title: POI Lookup
tag: [guide, android, geo, poi-lookup]
ref: 3-sdk-android-geo-poi-lookup
---

POI Lookup API provides basic information of POI(scenic spot, tide stations, currents stations, etc.)

| Interface Code| Interface  | Class |
| ----------- | --------------- | ---------- |
| getGeoPoiLookup| POI lookup  | GeoPoiBean |

### Parameter

{% include params.html p="location-geo geo-type city number lang-sdk" %}

### Sample Code

```java
QWeather.getGeoPoiLookup(Context context, String location, String city, int number, Type type, Lang lang, final OnResultGeoPoiListener listener);

QWeather.getGeoPoiLookup(Context context, String location, Type type, final QWeather.OnResultGeoPoiListener listener);
```

### Properties

Properties of GeoPoiBean

| Property | Description | Example |
| ---------- | -------- | --------------- |
| getCode | Status code, please refer to [Status Code](/en/docs/resource/status-code/) | Code |
| getPoiList | City data | List&lt;Poi&gt; |


**Refer**

| Property | Description | Example |
| -------------- | ------------ | ------------------ |
| getSourcesList | Data source and other statements | qweather.com |
| getLicenseList | Data license | commercial license |


**Poi**

| Property | Description | Example |
| ------------ | ------------------------------------ ----------------------------- | --------- |
| getName | POI name | Nanshan District |
| getId | Location ID | 101280604 |
| getLon | Longitude of the POI | 22.53122 |
| getLat | Latitude of the POI | 113.92942 |
| getAdm2 | Name of the superior administrative division of the POI | Shenzhen |
| getAdm1 | The first-level administrative region to which the POI belongs | Guangdong Province |
| getCountry | Country name of the POI | China |
| getTz | [Timezone](/en/docs/resource/glossary/#timezone) of the POI | Asia/Shanghai |
| getUtcOffset | The number of hours offset between local time and UTC time, refer to [UTC-Offset](/en/docs/resource/glossary/#utc-offset) | +08:00 |
| getIsDst | Is the location currently observing Daylight Saving time<br />`1` in daylight saving time <br /> `0` not in daylight saving time | 0 |
| getType | POI type | scenic |
| getRank | [Location Rank](/en/docs/resource/glossary/#rank) | 10 |