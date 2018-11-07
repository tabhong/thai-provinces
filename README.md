# thai-provinces
Determine if lat,lng is inside which province (a polygon with a ray intersection counting algorithm) that located in Thailand 

This module casts a ray from the inquiry point and counts intersections,
based on
[this algorithm](http://www.ecse.rpi.edu/Homepages/wrf/Research/Short_Notes/pnpoly.html).
and inside by James Halliday [point-in-polygon](https://github.com/substack/point-in-polygon).

# example

``` js
let thaiProvinces = require('thai-provinces');
console.log(thaiProvinces.findProvinceByLatlng(6.246567, 102.010678));

```

output:

```
{ location: { lat: 6.246567, lng: 102.010678 },
  status: 200,
  province: { name: 'นราธิวาส', district: 'ตากใบ' } }
```

# methods

``` js
let thaiProvinces = require('thai-provinces');
thaiProvinces.findProvinceByLatlng(6.246567, 102.010678);
```

## findProvinceByLatlng(lat, lng)

Return whether `lat`,`lng` is contained in which Thai's province.

`lat` latitude.

`lat` longitude.

# install

```
npm install thai-provinces
```

# license

MIT
