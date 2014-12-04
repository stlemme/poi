Permanent POIs, such as public places, will not have any time constraints. On the other hand, POIs representing an event, which happens only once, may use a time constraint to express the timeframe of this event by the use of validFrom and validThrough. Furthermore, for business it might be relevant to provide information about the opening hours. Thus, it is possible to attach opening hour specifications to express service times as intervals between open and close point in times. Irregular business hours or reoccurring events can be provided through multiple time constraints attached to the POI. It is also possible to provide particular opening hours for school holidays using a time constraint especially for this period.

Attributes of type TimeConstraint:
* opening_hours : array of type OpeningHourSpecification
* valid_from : type [[DateTime|UtilityTypes#DateTime]]
* valid_through : type [[DateTime|UtilityTypes#DateTime]]

Attributes of type OpeningHourSpecification:
* day_of_week : enum {
    monday, tuesday, wednesday, thursday, friday,
    saturday, sunday, public_holidays, weekday
}
* opens : type [[Time|UtilityTypes#Time]]
* closes : type [[Time|UtilityTypes#Time]]


***

JSON - a new fountain which will become available in future at 4th of December
<pre>
{
    "id": "5540b5d2-0909-4b0a-8a69-5ec3a64dc3d7",
    "contents": [
        {
            "type": "name",
            "name": "Bismarck-Brunnen"
        }
    ],
    "time_constraints": [
        {
            "valid_from": "2013-12-04T14:00+01:00"
        }
    ],
    "source": {
        "href": "http://url-to.this/poi/provider/5540b5d2-0909-4b0a-8a69-5ec3a64dc3d7"
    }
}
</pre>

JSON - a 3 days festival in 2013
<pre>
{
    "id": "5540b5d2-0909-4b0a-8a69-5ec3a64dc3d8",
    "contents": [
        {
            "type": "name",
            "name": "Rock im Park 2013"
        }
    ],
    "time_constraints": [
        {
            "valid_from": "2013-06-07"
            "valid_through": "2013-06-09"
        }
    ],
    "source": {
        "href": "http://url-to.this/poi/provider/5540b5d2-0909-4b0a-8a69-5ec3a64dc3d8"
    }
}
</pre>

JSON - a local car rental business
<pre>
{
    "id": "5540b5d2-0909-4b0a-8a69-5ec3a64dc3d9",
    "contents": [
        {
            "type": "name",
            "name": "RYC - Rent Your Car"
        }
    ],
    "time_constraints": [
        {
            "opening_hours": [
                {
                    "day_of_week": "weekday",
                    "opens": "09:00+01:00",
                    "closes": "18:00+01:00"
                },
                {
                    "day_of_week": "saturday",
                    "opens": "09:00+01:00",
                    "closes": "14:00+01:00"
                }
            ],
            "valid_through": "2014-05-31"
        }
    ],
    "source": {
        "href": "http://url-to.this/poi/provider/5540b5d2-0909-4b0a-8a69-5ec3a64dc3d9"
    }
}
</pre>

JSON - a local bar
<pre>
{
    "id": "5540b5d2-0909-4b0a-8a69-5ec3a64dc3da",
    "contents": [
        {
            "type": "name",
            "name": "Kneipe Pur"
        }
    ],
    "time_constraints": [
        {
            "opening_hours": [
                {
                    "day_of_week": "wednesday",
                    "opens": "18:00+01:00",
                    "closes": "23:00+01:00"
                },
                {
                    "day_of_week": "friday",
                    "opens": "20:00+01:00"
                },
                {
                    "day_of_week": "saturday",
                    "opens": "20:00+01:00"
                }
            ]
        }
    ],
    "source": {
        "href": "http://url-to.this/poi/provider/5540b5d2-0909-4b0a-8a69-5ec3a64dc3da"
    }
}
</pre>