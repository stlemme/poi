We reference the data source of a POI or parts of a POI such as specific content. Thereby, following information are provided, which are almost all not mandatory:
* author – one person or a provider,
* publisher – in case of user generated content this should be the provider,
* license – indicates the possible usage or contains the copyright notice,
* href – is a fully qualified URL to retrieve the POI or this part of the POI (self-reference)
* created – timestamp of the creation
* updated – timestamp of the last modification
* revision – indicates the number of changes

At least the POI need to provide this data source reference information including the self-reference attribute (href). For compound POIs it is possible to overwrite some of these information by providing specific ones for a component, e.g. an image as part of the attached content. Thus, it is possible to retrieve updated information for a POI by querying several providers using different URLs.

Attributes of type DataSource:
* author : string
* publisher : string
* license : string
* href : type [[URL|UtilityTypes#URL]]
* created : type [[DateTime|UtilityTypes#DateTime]]
* updated : type [[DateTime|UtilityTypes#DateTime]]
* revision : int
* change_frequency : enum {
      always, hourly, daily, weekly, monthly, yearly, never
  }

Attributes of type MainDataSource { DataSource }:
* **href : type [[URL|UtilityTypes#URL]]**

***

JSON
<pre>
{
    "id": "5540b5d2-0909-4b0a-8a69-5ec3a64dc3d7",
    "source": {
        "href": "http://url-to.this/poi/provider/5540b5d2-0909-4b0a-8a69-5ec3a64dc3d7"
    }
}
</pre>
<pre>
{
    "id": "5540b5d2-0909-4b0a-8a69-5ec3a64dc3d7",
    "contents": [
        {
            "type": "image",
            "resource": "http://url-to.the/attached/image",
            "source": {
                "author": "Fritz",
                "created": "2013-08-28T14:50+01:00",
                "href": "http://url-to.another/poi/provider/5540b5d2-0909-4b0a-8a69-5ec3a64dc3d7"
            }
        }
    ],
    "source": {
        "author": "Emil",
        "publisher": "My POI Provider",
        "href": "http://url-to.this/poi/provider/5540b5d2-0909-4b0a-8a69-5ec3a64dc3d7"
    }
}
</pre>