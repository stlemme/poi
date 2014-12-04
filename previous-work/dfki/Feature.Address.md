The postal or civic address is a unique identifier for a location. Hence, we allow to describe to localization of a POI using an address. Therefore, we utilize the fashion of Google Places to specify the components of the address. https://developers.google.com/places/documentation/details#PlaceDetailsResults

Attributes of type Feature.Address { Feature( method = address ) }:
* **components : array of type AddressComponent**
* formatted : string

Attributes of type AddressComponent
* **types : an array of strings** - indicating the type of the address component
* **long_name : string** - is the full text description or name of the address component.
* short_name : string - is an abbreviated textual name for the address component, if available. For example, an address component for the state of Alaska may have a long_name of "Alaska" and a short_name of "AK" using the 2-letter postal abbreviation.


***

JSON
<pre>
{
}
</pre>