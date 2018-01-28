Using geocoder:

In this example, we use geocoder to look up any part of an address.
In this project, geocoder will give us details about the address such as:

latitude, longitude, country, postal code, neighborhood, and more; just from inserting a piece of the complete address!

Here, I am not using a server to power the project, and everything is done within one html file: geocoder.html.

I am also using axios to make the request to the google geocoder API for convenience.

    
All information required comes back from  the "results" object that Google has already structured for us (info here has been filled with example data):

            {
               "results" : [
                  {
                     "address_components" : [
                        {
                           "long_name" : "1600",
                           "short_name" : "1600",
                           "types" : [ "street_number" ]
                        },
                        {
                           "long_name" : "Amphitheatre Pkwy",
                           "short_name" : "Amphitheatre Pkwy",
                           "types" : [ "route" ]
                        },
                        {
                           "long_name" : "Mountain View",
                           "short_name" : "Mountain View",
                           "types" : [ "locality", "political" ]
                        },
                        {
                           "long_name" : "Santa Clara County",
                           "short_name" : "Santa Clara County",
                           "types" : [ "administrative_area_level_2", "political" ]
                        },
                        {
                           "long_name" : "California",
                           "short_name" : "CA",
                           "types" : [ "administrative_area_level_1", "political" ]
                        },
                        {
                           "long_name" : "United States",
                           "short_name" : "US",
                           "types" : [ "country", "political" ]
                        },
                        {
                           "long_name" : "94043",
                           "short_name" : "94043",
                           "types" : [ "postal_code" ]
                        }
                     ],
                     "formatted_address" : "1600 Amphitheatre Parkway, Mountain View, CA 94043, USA",
                     "geometry" : {
                        "location" : {
                           "lat" : 37.4224764,
                           "lng" : -122.0842499
                        },
                        "location_type" : "ROOFTOP",
                        "viewport" : {
                           "northeast" : {
                              "lat" : 37.4238253802915,
                              "lng" : -122.0829009197085
                           },
                           "southwest" : {
                              "lat" : 37.4211274197085,
                              "lng" : -122.0855988802915
                           }
                        }
                     },
                     "place_id" : "ChIJ2eUgeAK6j4ARbn5u_wAGqWA",
                     "types" : [ "street_address" ]
                  }
               ],
               "status" : "OK"
            }

This way, we can get a full formatted_address, certain components of the address like route, street number, etc, and the geometry (lat, lng)!
        