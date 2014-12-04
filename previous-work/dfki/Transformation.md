The transformation wraps a combination of a translation, a rotation and a scaling. All is combined to one 4x4 matrix. Each field has default values and a valid transformation is described by any of the fields. Thereby, the matrix field is always derived from the other fields if present. If no field is present, the transformation represents the identity.

Attributes of type Transformation:
* translation : type [[vec2x|UtilityTypes#vec2x]] (default = (0.0, 0.0, 0.0))
* rotation : type [[quaternion|UtilityTypes#quaternion]] (default = [1.0, (0.0, 0.0, 0.0)])
* scaling : type [[vec2x|UtilityTypes#vec2x]] (default = [1.0, 1.0, 1.0])
* matrix : type [[Matrix|UtilityTypes#Matrix]] (= Mat.translation * Mat.rotation * Mat.scaling)

***

JSON
<pre>
{
}
</pre>