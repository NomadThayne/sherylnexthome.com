# JSON-LD Structured Data (Schema.org)
# Paste each <script> block just before </body> on the corresponding page

---

## index.html — LocalBusiness + RealEstateAgent

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "RealEstateAgent",
      "@id": "https://sherylnexthome.com/#agent",
      "name": "Sheryl Whipple",
      "url": "https://sherylnexthome.com/",
      "telephone": "+18059017546",
      "email": "sherylw.realestate@gmail.com",
      "image": "https://sherylnexthome.com/images/sheryl.jpg",
      "description": "Ojai Valley real estate specialist with 25 years of local experience. Buyer broker, residential, single-family homes, vacation rentals, and relocation.",
      "address": {
        "@type": "PostalAddress",
        "streetAddress": "307 A East Matilija St",
        "addressLocality": "Ojai",
        "addressRegion": "CA",
        "postalCode": "93023",
        "addressCountry": "US"
      },
      "geo": {
        "@type": "GeoCoordinates",
        "latitude": 34.4480,
        "longitude": -119.2429
      },
      "areaServed": {
        "@type": "City",
        "name": "Ojai",
        "sameAs": "https://en.wikipedia.org/wiki/Ojai,_California"
      },
      "memberOf": {
        "@type": "Organization",
        "name": "NextHome Pacific Coast Realty",
        "url": "https://www.nexthomepacificcoastrealty.com"
      },
      "hasCredential": "CalDRE #01379424",
      "sameAs": [
        "https://www.nexthomepacificcoastrealty.com"
      ]
    },
    {
      "@type": "WebSite",
      "@id": "https://sherylnexthome.com/#website",
      "url": "https://sherylnexthome.com/",
      "name": "Ojai Homes · Sheryl Whipple · NextHome",
      "description": "Homes for sale and rent in the Ojai Valley, California.",
      "publisher": {
        "@id": "https://sherylnexthome.com/#agent"
      }
    }
  ]
}
</script>
```

---

## macdonald.html — RealEstateListing

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "RealEstateListing",
  "@id": "https://sherylnexthome.com/macdonald.html",
  "name": "12750 Macdonald Drive, Ojai, CA 93023",
  "url": "https://sherylnexthome.com/macdonald.html",
  "description": "French Provincial estate designed by architect Braden Sterling. 5 bedrooms, 3.5 bathrooms, 4,244 sq ft on 2.1 private acres with panoramic Topa Topa Mountain views, resort-style pool, spa, fire pit, rose gardens, fruit orchard, and direct access to Ojai River Preserve trails and Los Padres National Forest.",
  "image": [
    "https://sherylnexthome.com/images/12750%20Macdonald%20Drive/macdonald1.jpg"
  ],
  "offers": {
    "@type": "Offer",
    "price": "3575000",
    "priceCurrency": "USD",
    "availability": "https://schema.org/InStock",
    "seller": {
      "@type": "RealEstateAgent",
      "name": "Sheryl Whipple",
      "telephone": "+18059017546",
      "url": "https://sherylnexthome.com/"
    }
  },
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "12750 Macdonald Drive",
    "addressLocality": "Ojai",
    "addressRegion": "CA",
    "postalCode": "93023",
    "addressCountry": "US"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 34.4721,
    "longitude": -119.3012
  },
  "numberOfRooms": 5,
  "floorSize": {
    "@type": "QuantitativeValue",
    "value": 4244,
    "unitCode": "FTK"
  },
  "lotSize": {
    "@type": "QuantitativeValue",
    "value": 2.1,
    "unitText": "acres"
  },
  "numberOfBathroomsTotal": 4,
  "identifier": {
    "@type": "PropertyValue",
    "name": "MLS",
    "value": "V1-33494"
  },
  "additionalProperty": [
    { "@type": "PropertyValue", "name": "Property Type", "value": "Single Family Home" },
    { "@type": "PropertyValue", "name": "Style", "value": "French Provincial" },
    { "@type": "PropertyValue", "name": "Pool", "value": "Yes" },
    { "@type": "PropertyValue", "name": "Horses OK", "value": "Yes" }
  ]
}
</script>
```

---

## mcnell.html — RealEstateListing

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "RealEstateListing",
  "@id": "https://sherylnexthome.com/mcnell.html",
  "name": "757 McNell Road, Ojai, CA 93023",
  "url": "https://sherylnexthome.com/mcnell.html",
  "description": "Charming single-family home on one of Ojai's most beloved East End streets. 3 bedrooms, 2 bathrooms, 1,880 sq ft on 0.32 acres. Oak-canopied street with mountain views, close to Ojai Valley Trail and downtown Ojai.",
  "image": [
    "https://sherylnexthome.com/images/mcnell/mcnell.jpg"
  ],
  "offers": {
    "@type": "Offer",
    "price": "1970000",
    "priceCurrency": "USD",
    "availability": "https://schema.org/InStock",
    "seller": {
      "@type": "RealEstateAgent",
      "name": "Sheryl Whipple",
      "telephone": "+18059017546",
      "url": "https://sherylnexthome.com/"
    }
  },
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "757 McNell Road",
    "addressLocality": "Ojai",
    "addressRegion": "CA",
    "postalCode": "93023",
    "addressCountry": "US"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 34.4468,
    "longitude": -119.2201
  },
  "numberOfRooms": 3,
  "floorSize": {
    "@type": "QuantitativeValue",
    "value": 1880,
    "unitCode": "FTK"
  },
  "lotSize": {
    "@type": "QuantitativeValue",
    "value": 0.32,
    "unitText": "acres"
  },
  "numberOfBathroomsTotal": 2,
  "identifier": {
    "@type": "PropertyValue",
    "name": "MLS",
    "value": "V1-35424"
  },
  "additionalProperty": [
    { "@type": "PropertyValue", "name": "Property Type", "value": "Single Family Home" },
    { "@type": "PropertyValue", "name": "Neighborhood", "value": "East End" }
  ]
}
</script>
```

---

## resources.html — WebPage

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebPage",
  "name": "Ojai Valley Resources · Local Guide for Residents & Buyers",
  "url": "https://sherylnexthome.com/resources.html",
  "description": "Comprehensive local resource guide for Ojai Valley residents and buyers: utilities, schools, medical, dining, government, outdoors, arts, and transit.",
  "inLanguage": "en-US",
  "isPartOf": {
    "@type": "WebSite",
    "url": "https://sherylnexthome.com/",
    "name": "Ojai Homes · Sheryl Whipple · NextHome"
  },
  "author": {
    "@type": "RealEstateAgent",
    "name": "Sheryl Whipple",
    "url": "https://sherylnexthome.com/"
  },
  "about": {
    "@type": "City",
    "name": "Ojai",
    "containedInPlace": {
      "@type": "AdministrativeArea",
      "name": "Ventura County",
      "containedInPlace": {
        "@type": "State",
        "name": "California"
      }
    }
  }
}
</script>
```
