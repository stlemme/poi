We utilize features to find, locate and map the POI. A feature is dedicated to a specific positioning method, such as GPS, Wifi-based or by address, marker tracking, fast feature tracking, etc. It holds the respective parameters and describes the transformation from the positioning method’s coordinate system to the local coordinate system of the POI. Thus, a feature specifies its dedicated positioning method with their parameters, the transformation to the POI’s reference coordinate system using a matrix, probably a deviation of the positioning method in this spatial area and maybe the data source of this feature.

Attributes of type Feature:
* **method : enum {
      wgs84, etrs89, address, gln, nyidmarker, qrcode,
      relative, soft, ...
  }**
* transformation : type [[Transformation]] (default = identity)
* deviation : type vec2x
* source : type [[DataSource]]

The list of supported features so far contains:
* [[Feature.WGS84]]
* [[Feature.ETRS89]]
* [[Feature.Address]]
* [[Feature.GLN]]
* [[Feature.NyID]]
* [[Feature.QRCode]]
* [[Feature.Relative]]
* [[Feature.Soft]]
