# Kern Valley Places
[![Super Linter](https://github.com/kernvalley/places/workflows/Lint%20Code%20Base/badge.svg)](https://github.com/kernvalley/places/actions?query=workflow%3A%22Lint+Code+Base%22)
[![GitHub license](https://img.shields.io/github/license/kernvalley/places.svg)](https://github.com/kernvalley/places/blob/master/LICENSE)
[![GitHub issues](https://img.shields.io/github/issues/kernvalley/places.svg)](https://github.com/kernvalley/places/issues)
[![GitHub pull requests](https://img.shields.io/github/issues-pr/kernvalley/places.svg)](https://github.com/kernvalley/places/pulls)
[![GitHub last commit](https://img.shields.io/github/last-commit/kernvalley/places.svg)](https://github.com/kernvalley/places/commits/master)
[![GitHub release](https://img.shields.io/github/release/kernvalley/places.svg)](https://github.com/kernvalley/places/releases)

![GitHub followers](https://img.shields.io/github/followers/kernvalley.svg?style=social)
![GitHub forks](https://img.shields.io/github/forks/kernvalley/places.svg?style=social)
![GitHub stars](https://img.shields.io/github/stars/kernvalley/places.svg?style=social)
[![Twitter Follow](https://img.shields.io/twitter/follow/kern_valley.svg?style=social)](https://twitter.com/kern_valley)

- - -
> This is a collection of data for places around the Kern River Valley. All data
> is structured according to specifications on [schema.org](https://schema.org).
> All data is to be stored in YAML (`.yml`) files and **MUST** contain a top-level
> `"@context"` and set every `"@type"`. The minimal required fields are:
- `"@type"`
- `name`
- `identifier` (*set to a UUID*)
- `geo` containing `"@type": GeoCoordinates`, `latitude`, and `longitude`

## Helpful Links:
- [Code of Conduct](./.github/CODE_OF_CONDUCT.md)
- [Contributing](./.github/CONTRIBUTING.md)
- https://schema.org/Place
- https://schema.org/LocalBusiness
- https://schema.org/Restaurant
- https://search.google.com/test/rich-results

**Note**: for every `"@type"`, there is a corresponding specification on schema.org.
For `"@type": "ImageObject"`, documentation may be found at `https://schema.org/ImageObject`.

For testing purposes, you must use JSON formatting and enclose the object with:
```html
<script type="application/ld+json">
{
  "@context": "https://schema.org"
}
</script>
```

## YAML Sample Data (*Disneyland*)
```yaml
---
- "@context": https://schema.org
  "@type": AmusementPark
  name: Disneyland
  identifier: fe0b6813-b195-4ff8-92cb-2dfa5e572292
  url: https://disneyland.disney.go.com
  telephone: 714-781-4636
  priceRange: "$$$$$"
  sameAs:
    - https://en.wikipedia.org/wiki/Disneyland
  image:
    - "@type": ImageObject
      url: https://i.imgur.com/r2HcDjk.jpg
      height: 600
      width: 800
      encodingFormat: image/jpeg
    - "@type": ImageObject
      url: https://i.imgur.com/r2HcDjkm.jpg
      height: 240
      width: 320
      encodingFormat: image/jpeg
  logo:
    - "@type": ImageObject
      url: https://upload.wikimedia.org/wikipedia/commons/1/13/Disneyland_Park_Logo.svg
      width: 174.635
      height: 47.781
      encodingFormat: image/svg+xml
  address:
    "@type": PostalAddress
    streetAddress: 1313 South Harbor Boulevard
    addressLocality: Anaheim
    addressRegion: CA
    postalCode: 92802,
    url: https://openstreetmap.org/way/592176675
  geo:
    "@type": GeoCoordinates
    latitude: 33.813668
    longitude: -117.919711
    elevation: 42
  openingHoursSpecification:
    - "@type": OpeningHoursSpecification
      dayOfWeek: Sunday
      opens: '09:00'
      closes: '21:00'
    - "@type": OpeningHoursSpecification
      dayOfWeek: Monday
      opens: '09:00'
      closes: '19:00'
    - "@type": OpeningHoursSpecification
      dayOfWeek: Tuesday
      opens: '09:00'
      closes: '19:00'
    - "@type": OpeningHoursSpecification
      dayOfWeek: Wednesday
      opens: '09:00'
      closes: '19:00'
    - "@type": OpeningHoursSpecification
      dayOfWeek: Thursday
      opens: '09:00'
      closes: '19:00'
    - "@type": OpeningHoursSpecification
      dayOfWeek: Friday
      opens: '09:00'
      closes: '21:00'
    - "@type": OpeningHoursSpecification
      dayOfWeek: Saturday
      opens: '09:00'
      closes: '21:00'
```

## JSON Sample Data (*Disneyland*)
```json
[{
  "@context": "https://schema.org",
  "@type": "AmusementPark",
  "name": "Disneyland",
  "identifier": "fe0b6813-b195-4ff8-92cb-2dfa5e572292",
  "url": "https://disneyland.disney.go.com",
  "telephone": "714-781-4636",
  "priceRange": "$$$$$",
  "sameAs": [
    "https://en.wikipedia.org/wiki/Disneyland"
  ],
  "image": [{
    "@type": "ImageObject",
    "url": "https://i.imgur.com/r2HcDjk.jpg",
    "height": 600,
    "width": 800,
    "encodingFormat": "image/jpeg"
  }, {
    "@type": "ImageObject",
    "url": "https://i.imgur.com/r2HcDjkm.jpg",
    "height": 240,
    "width": 320,
    "encodingFormat": "image/jpeg"
  }],
  "logo": [{
    "@type": "ImageObject",
    "url": "https://upload.wikimedia.org/wikipedia/commons/1/13/Disneyland_Park_Logo.svg",
    "width": 174.635,
    "height": 47.781,
    "encodingFormat": "image/svg+xml"
  }],
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "1313 South Harbor Boulevard",
    "addressLocality": "Anaheim",
    "addressRegion": "CA",
    "postalCode": 92802,
    "url": "https://openstreetmap.org/way/592176675"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 33.813668,
    "longitude": -117.919711,
    "elevation": 42
  },
  "openingHoursSpecification": [{
    "@type": "OpeningHoursSpecification",
    "dayOfWeek": "Sunday",
    "opens": "09:00",
    "closes": "21:00"
  }, {
    "@type": "OpeningHoursSpecification",
    "dayOfWeek": "Monday",
    "opens": "09:00",
    "closes": "19:00"
  }, {
    "@type": "OpeningHoursSpecification",
    "dayOfWeek": "Tuesday",
    "opens": "09:00",
    "closes": "19:00"
  }, {
    "@type": "OpeningHoursSpecification",
    "dayOfWeek": "Wednesday",
    "opens": "09:00",
    "closes": "19:00"
  }, {
    "@type": "OpeningHoursSpecification",
    "dayOfWeek": "Thursday",
    "opens": "09:00",
    "closes": "19:00"
  }, {
    "@type": "OpeningHoursSpecification",
    "dayOfWeek": "Friday",
    "opens": "09:00",
    "closes": "21:00"
  }, {
    "@type": "OpeningHoursSpecification",
    "dayOfWeek": "Saturday",
    "opens": "09:00",
    "closes": "21:00"
  }]
}]
```
