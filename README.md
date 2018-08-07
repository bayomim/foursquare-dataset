# foursquare-dataset
A Foursquare dataset for contextual suggestion

A dataset that we've collected for our participation in TREC 2016 Contextual Suggestion track.
https://sites.google.com/site/treccontext/

The dataset comprises 228,778 attractions such as: Parks, Restaurants, Meusums, etc.
    
    Update: 2018-07-23 - a new set of 969 attractions are now added
    the new dataset contains 229,747 attractions

The dataset is in JSON format and it was collected from 2017-01-30 to 2017-02-22.

    Update: the last 969 attractions in the dataset were collected on 2018-07-23

Attractions in this dataset are from different cities in the US. 

The dataset is for research use ONLY.

Please cite our paper if you publish material based on this dataset.

    @inproceedings{bayomi2016adapt_tcd,
       title={ADAPT\_TCD: An Ontology-Based Context Aware Approach for Contextual Suggestion.},
       author={Bayomi, Mostafa and Lawless, S{\'e}amus},
       booktitle={TREC},
       year={2016}
     }
Our paper is available here:
https://trec.nist.gov/pubs/trec25/papers/ADAPT_TCD-CX.pdf

Each object in the JSON file has data from the contextual suggestion track (e.g. attractioh id, city, city location., etc.)

Each object contains a "foursquare" object that has all the data associated with the attraction on Foursquare including users' reviews.

User names and Ids are anonymised.

The dataset is available here:

https://drive.google.com/file/d/1rk8QxxR9GhxcHr7ZRXI8oD_5a6UijDW2/view?usp=sharing

A sample of an object in the dataset is as follows:

    {"_id": {"$oid":"58907c200eb9c5a0205f634f"}, // a unique id assigned by MongoDB.
    "id":"TRECCS-00652087-350", // Attraction's ID provided by TREC Contextual Suggestion track
    "orig_url":"http://www.yelp.com/biz/norm-waitt-sr-ymca-south-sioux-city", // Attraction's URL provided by TREC Contextual Suggestion track
    "title":"Norm Waitt Sr YMCA", // Attraction's title provided by TREC Contextual Suggestion track
    "city_id":350, // Attraction's City ID in the TREC Contextual Suggestion track dataset
    "city_name":"Sioux City", // Attraction's City name in the TREC Contextual Suggestion track dataset
    "state":"IA", // Attraction's state in the TREC Contextual Suggestion track dataset
    "lat":42.49999, // Latitude of the CITY (not the attraction) in the TREC Contextual Suggestion track dataset
    "long":-96.40031, // Longitude of the CITY (not the attraction) in the TREC Contextual Suggestion track dataset
    "foursquare":{ // This is the data we collected from Foursquare about this attraction
          "timestamp":{"$date":"2017-01-30T15:51:11.287Z"}, // The time when the data was collected
          "title":"Norm Waitt Sr. YMCA", //  Attraction's title in Foursquare
          "foursqaure_url":"https://foursquare.com/v/norm-waitt-sr-ymca/4c61d1ac4be3b7138adcd3e8", //  Attraction's URL in Foursquare. Note the last part of the URL is the attraction's ID in Foursquare
          "rating":8.7, // Attraction's rating
          "ratingCount":17,// Number of users who gave rating to this attraction in Foursquare
          "reviewCount":3, // Number of users who wrote reviews on this attraction in Foursquare
          "photosCount":0, // Number of photos associated with this  attraction 
          "categories":["Gym / Fitness Center"], // Category of the attraction
          "openingTimes":[ // Open and close times
                {"days":"Mon–Fri","hours":["5:00 AM–10:00 PM"]},
                {"days":"Sat","hours":["6:00 AM–6:00 PM"]},
                {"days":"Sun","hours":["Noon–6:00 PM"]}],
                "venue_url":"nwsymca.org", // original URL of the attraction
                "address":"601 Riverview DrSouth Sioux City, NE 68776United States",
                "description":"The NWSYMCA has been an essential part of Siouxland community for over 125 years. As a diverse, non-profit organization, all members, volunteers, staff \u0026 donors are joined together by the shared commitment youth development, healthy living and social responsibility.", // a description for the attraction in Foursquare
                "otherLocations":{"length":0,"locations":[]},// If this attraction has other locations
                "features":[// What features this attraction has
                      {"feature":"Credit Cards","value":"Yes"},
                      {"feature":"Wi-Fi","value":"Free"}],
                "menus":[],// What dishes are in the menue (if a restaurant)
                "drinks":[],// What drinks are in the menue (if a restaurant)
                "tagCloudArray":[], // Prominent keywords etracted from the users' reviews
                "reviews":[ // users' reviews
                    {
                    "userName":2, // userName and userId have the same number. This is the anonymous ID 
                    "userId":2,
                    "tipDate":"January 10, 2016",// the date where this review was written
                    "tipText":"Great classes for non-members. We really enjoy aqua tots with our son." // The review text
                    },
                    {
                    "userName":"3",
                    "userId":"3",
                    "tipDate":"March 29, 2011",
                    "tipText":"Need a new workout? Try a group class (power, step, ride, centergy) ... there's something for everyone."
                    },
                    .... // more reviews
                    ]} // End of "foursquare" object
                    }
