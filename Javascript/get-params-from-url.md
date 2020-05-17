# Get params from URL

A nice way of getting and setting params in a url is to use the std URL object with 
``` javascript
const urlObj = new URL('http://someValidUrl.com?v=1'); 

let foo = urlObj.searchParams.get('foo'); // = 1
urlOj.searchParms.set('bar', 2);
```
