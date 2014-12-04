Additionally, the structure component holds information about the bounding volume of this shape. This is either a bounding cylinder or a bounding circle and can be derived from the “real” shape. Alternatively, it can be provided by the POI author and include some height in addition to the flat outline of a building.

Attributes of type Bounds:
* **center : type [[vec2x|UtilityTypes#vec2x]]**
* **radius : float**
* height : float (default = 0.0)

***

JSON
<pre>
{
    "id": "5540b5d2-0909-4b0a-8a69-5ec3a64dc3d7",
    "structure": {
        "bounds": {
            "center": [0, 0],
            "radius": 0
        }
    },
    "source": {
        "href": "http://url-to.this/poi/provider"
    }
}
</pre>
