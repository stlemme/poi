The shape is given as a representation within the local reference coordinate system of the POI. This representations is defined by a type, an array of vertices and an optional array of indices. Since the usage of the z-component in the coordinates is optional, a parameter indicates if the vertices include elevation data. As types for shape representation are defined so far:
* **Point** – e.g. for a specific place or small object.
The array of vertices contains 2 or 3 floats.
* **Path** – e.g. for a hiking track, a promenade or a street.
The array of vertices contains 2*n or 3*n floats – depending on the elevation data indicator – and they are connected in the provided order to a line string.
* **Polygon** – e.g. for a park, region or building complex.
The array of vertices contains 2*n or 3*n floats – depending on the elevation data indicator – and they are connected in the provided order to enclose a polygon by adding an edge between the last and the first vertex.

We suggest to omit the usage of elevation data for shapes of type polygon unless you strongly ensure the planarity of the polygon – otherwise it will cumber a probable triangulation. Later extension for types of representations could be triangles to represent complete buildings instead of only the outline, for instance. In that case, this will take advantage of the optional array of indices, which is not yet necessary for the current types.

Attributes of type Shape:
* **type : enum { point, path, polygon }**
* elevation : boolean (default = false)
* **vertices : array of float (length of 2n or 3n; point: n = 1)**

***

JSON
<pre>
{
}
</pre>