A POI entity is of type POI and consists of several components providing capabilities to the POI format.
We use several data types and we will specify them in the following sections except basic data types, which are string, float, int, array, boolean, enum, char, bit. The specification of these data types will be done during the mapping of the actual transfer format.
Attributes in bold font are mandatory attributes of the explained type, like id and source for the POI type. Furthermore, there is some kind of inheritance used, which is expressed by
Subtype { BaseType ( baseattribute = value ) }.

Attributes of type POI:
* **id / _id : type [[UUID]]**
* structure : type [[Structure]]
* features : array of type [[Feature]]
* contents : array of type [[Content]]
* times : array of type [[TimeConstraint]]
* **source : type [[MainDataSource|DataSource]]**
* relations : array of type [[Relation]]
* meta : array of type [[Metadata]]

***

JSON
<pre>
{
    "id": "5540b5d2-0909-4b0a-8a69-5ec3a64dc3d7",
    "source": {
        "href": "http://url-to.this/poi/provider"
    }
}
</pre>