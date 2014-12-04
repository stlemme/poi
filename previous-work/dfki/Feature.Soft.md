We introduce some kind of meta localization for POIs using soft coordinates relative to another POIs. Therefore, we use human-readable instructions as description to navigate the user to a specific POI, such as “Third floor, second door on the left side”. This enables, for instance, a naïve implementation of indoor POIs.

Attributes of type Feature.Soft { Feature( method = soft ) }:
* **reference : [[POIReference]]**
* start_position : type vec2x
* **instructions : array of string**

***

JSON
<pre>
{
}
</pre>