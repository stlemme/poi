Several geographical coordinate reference systems are utilized in practice. One of the most used is the WGS84 coordinate system – usually known as GPS coordinates. Indeed, there are other coordinate systems used, such ETRS89 in the European area. We permit to use all of them to describe to localization of a POI. The constructed coordinate system in a point defined by any coordinates of a coordinate reference system has its x-axis and the y-axis as tangents of the reference rotation ellipsoid/cylinder and thereby, the y-axis pointing north and the x-axis pointing west. The z-axis is collinear to the surface normal of this ellipsoid/cylinder.

Attributes of type Feature.WGS84 { Feature( method = wgs84 ) }:
* **longitude : float**
* **latitude : float**
* elevation : float (default = ground-bound)

***

JSON
<pre>
{
}
</pre>