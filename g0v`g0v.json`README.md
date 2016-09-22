# g0v.json

The metadata specification for g0v projects.

``` js
// Get schema by version

import g0vJSON from "g0v.json";

const schema = new g0vJSON("v1").schema();

console.log(schema.properties);
```
